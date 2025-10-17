# ChatGPT API Demo Project

## Overview

Learn how to integrate OpenAI's ChatGPT API into a web application. This demo project teaches you the fundamentals of working with AI language models.

## What You'll Build

A simple chat interface that connects to OpenAI's GPT models, demonstrating:
- API authentication
- Sending prompts and receiving responses
- Streaming responses
- Managing conversation context
- Error handling
- Cost management

## Prerequisites

- Node.js installed
- Basic JavaScript/React knowledge
- OpenAI API account
- API key from [platform.openai.com](https://platform.openai.com)

## Learning Objectives

- Understand AI API authentication
- Make API requests to OpenAI
- Handle streaming responses
- Manage API costs
- Implement error handling
- Build conversational interfaces

## Quick Start

### 1. Get API Key
```
1. Go to platform.openai.com
2. Create account / Sign in
3. Navigate to API Keys section
4. Create new secret key
5. Copy and save it (you won't see it again!)
```

### 2. Setup Project
```bash
# Create project folder
mkdir chatgpt-demo
cd chatgpt-demo

# Initialize npm
npm init -y

# Install dependencies
npm install openai dotenv express cors
npm install -D nodemon
```

### 3. Create Files

#### .env
```
OPENAI_API_KEY=your_api_key_here
PORT=5000
```

#### server.js
```javascript
import 'dotenv/config';
import express from 'express';
import cors from 'cors';
import OpenAI from 'openai';

const app = express();
const port = process.env.PORT || 5000;

// Middleware
app.use(cors());
app.use(express.json());

// Initialize OpenAI
const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY
});

// Chat endpoint
app.post('/api/chat', async (req, res) => {
  try {
    const { message, conversationHistory = [] } = req.body;

    // Prepare messages
    const messages = [
      { role: 'system', content: 'You are a helpful assistant.' },
      ...conversationHistory,
      { role: 'user', content: message }
    ];

    // Call OpenAI API
    const completion = await openai.chat.completions.create({
      model: 'gpt-3.5-turbo',
      messages: messages,
      max_tokens: 500,
      temperature: 0.7
    });

    // Send response
    res.json({
      response: completion.choices[0].message.content,
      usage: completion.usage
    });

  } catch (error) {
    console.error('Error:', error.message);
    res.status(500).json({
      error: 'Failed to get response from AI',
      details: error.message
    });
  }
});

// Health check
app.get('/health', (req, res) => {
  res.json({ status: 'OK' });
});

app.listen(port, () => {
  console.log(`Server running on port ${port}`);
});
```

### 4. Run Server
```bash
node server.js
```

### 5. Test with curl
```bash
curl -X POST http://localhost:5000/api/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "Hello, how are you?"}'
```

## Key Concepts

### 1. API Authentication
```javascript
const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY
});
```

### 2. Message Format
```javascript
const messages = [
  {
    role: 'system',
    content: 'You are a helpful assistant.'
  },
  {
    role: 'user',
    content: 'What is JavaScript?'
  },
  {
    role: 'assistant',
    content: 'JavaScript is a programming language...'
  }
];
```

### 3. Model Parameters
```javascript
{
  model: 'gpt-3.5-turbo',  // or 'gpt-4'
  messages: messages,
  max_tokens: 500,         // Limit response length
  temperature: 0.7,        // 0-2, controls randomness
  top_p: 1,               // Alternative to temperature
  frequency_penalty: 0,    // -2 to 2
  presence_penalty: 0     // -2 to 2
}
```

### 4. Streaming Responses
```javascript
const stream = await openai.chat.completions.create({
  model: 'gpt-3.5-turbo',
  messages: messages,
  stream: true
});

for await (const chunk of stream) {
  const content = chunk.choices[0]?.delta?.content || '';
  process.stdout.write(content);
}
```

## Frontend Example (React)

```jsx
import { useState } from 'react';

function ChatApp() {
  const [messages, setMessages] = useState([]);
  const [input, setInput] = useState('');
  const [loading, setLoading] = useState(false);

  const sendMessage = async (e) => {
    e.preventDefault();
    if (!input.trim()) return;

    const userMessage = { role: 'user', content: input };
    setMessages([...messages, userMessage]);
    setInput('');
    setLoading(true);

    try {
      const response = await fetch('http://localhost:5000/api/chat', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify({
          message: input,
          conversationHistory: messages
        })
      });

      const data = await response.json();

      if (data.response) {
        setMessages(prev => [
          ...prev,
          { role: 'assistant', content: data.response }
        ]);
      }
    } catch (error) {
      console.error('Error:', error);
    } finally {
      setLoading(false);
    }
  };

  return (
    <div className="chat-container">
      <div className="messages">
        {messages.map((msg, idx) => (
          <div key={idx} className={`message ${msg.role}`}>
            <strong>{msg.role}:</strong> {msg.content}
          </div>
        ))}
        {loading && <div>AI is thinking...</div>}
      </div>

      <form onSubmit={sendMessage}>
        <input
          type="text"
          value={input}
          onChange={(e) => setInput(e.target.value)}
          placeholder="Type a message..."
          disabled={loading}
        />
        <button type="submit" disabled={loading}>
          Send
        </button>
      </form>
    </div>
  );
}

export default ChatApp;
```

## Cost Management

### Pricing (as of 2025)
- **GPT-3.5-turbo**: ~$0.002 per 1K tokens
- **GPT-4**: ~$0.03-0.06 per 1K tokens

### Tips to Reduce Costs
```javascript
// 1. Limit max_tokens
max_tokens: 500  // Instead of 2000

// 2. Use cheaper models for simple tasks
model: 'gpt-3.5-turbo'  // Instead of 'gpt-4'

// 3. Limit conversation history
conversationHistory: conversationHistory.slice(-5)  // Only last 5 messages

// 4. Implement rate limiting
// 5. Cache common responses
// 6. Set spending limits in OpenAI dashboard
```

## Error Handling

```javascript
app.post('/api/chat', async (req, res) => {
  try {
    const completion = await openai.chat.completions.create({...});
    res.json({ response: completion.choices[0].message.content });

  } catch (error) {
    if (error.code === 'insufficient_quota') {
      return res.status(429).json({
        error: 'API quota exceeded'
      });
    }

    if (error.code === 'rate_limit_exceeded') {
      return res.status(429).json({
        error: 'Too many requests'
      });
    }

    if (error.code === 'invalid_api_key') {
      return res.status(401).json({
        error: 'Invalid API key'
      });
    }

    res.status(500).json({
      error: 'Internal server error'
    });
  }
});
```

## Advanced Features

### 1. System Prompt Customization
```javascript
const systemPrompts = {
  helpful: 'You are a helpful assistant.',
  teacher: 'You are a patient teacher explaining concepts clearly.',
  coder: 'You are an expert programmer providing code solutions.',
  creative: 'You are a creative writer helping with storytelling.'
};
```

### 2. Function Calling
```javascript
const completion = await openai.chat.completions.create({
  model: 'gpt-3.5-turbo',
  messages: messages,
  functions: [
    {
      name: 'get_weather',
      description: 'Get weather for a location',
      parameters: {
        type: 'object',
        properties: {
          location: { type: 'string' }
        }
      }
    }
  ]
});
```

### 3. Token Counting
```javascript
import { encode } from 'gpt-tokenizer';

function countTokens(text) {
  return encode(text).length;
}

const tokens = countTokens('Hello, world!');
console.log(`Tokens: ${tokens}`);
```

## Practice Exercises

1. **Basic Chat**: Implement simple question-answer
2. **Conversation History**: Maintain context across messages
3. **Custom Personas**: Create different AI personalities
4. **Token Counter**: Display token usage per message
5. **Rate Limiting**: Implement request limits
6. **Streaming UI**: Show responses as they're generated

## Resources

- [OpenAI API Documentation](https://platform.openai.com/docs)
- [OpenAI Cookbook](https://github.com/openai/openai-cookbook)
- [Token Calculator](https://platform.openai.com/tokenizer)
- [Pricing Information](https://openai.com/pricing)

## Security Best Practices

1. ✅ Never expose API keys in frontend code
2. ✅ Use environment variables
3. ✅ Implement rate limiting
4. ✅ Validate user input
5. ✅ Set spending limits
6. ✅ Monitor usage in dashboard
7. ✅ Use HTTPS in production

## Common Issues & Solutions

### Issue: "Invalid API Key"
- Solution: Check .env file, ensure key is correct

### Issue: "Rate limit exceeded"
- Solution: Implement delays between requests

### Issue: "Quota exceeded"
- Solution: Check billing, add payment method

### Issue: High costs
- Solution: Use gpt-3.5-turbo, limit tokens, cache responses

---

This demo provides a foundation for building AI-powered chat applications. Experiment, learn, and build amazing things!
