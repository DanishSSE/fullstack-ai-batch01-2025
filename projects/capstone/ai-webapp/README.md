# Capstone Project: AI-Powered Web Application

## Project Overview

Build a full-stack web application that integrates AI capabilities using modern web technologies. This is your opportunity to showcase everything you've learned throughout the course and create a portfolio-worthy project.

## Timeline
- **Kickoff**: Week 21 (June 6, 2025)
- **Checkpoint 1**: Week 22 (June 13, 2025) - Proposal & Design
- **Checkpoint 2**: Week 23 (June 20, 2025) - MVP Demo
- **Final Submission**: June 22, 2025
- **Presentations**: June 20 & 23, 2025

## Learning Objectives

- Design and implement a full-stack application
- Integrate AI APIs into web applications
- Apply best practices for code organization
- Implement user authentication and authorization
- Deploy a production-ready application
- Present technical work effectively

## Project Requirements

### Minimum Technical Requirements

#### Frontend
- [ ] React.js application
- [ ] Responsive design (mobile + desktop)
- [ ] User authentication UI
- [ ] Loading states and error handling
- [ ] Modern, polished UI (consider using component libraries)

#### Backend
- [ ] Node.js with Express.js
- [ ] RESTful API design
- [ ] Database integration (MongoDB or PostgreSQL)
- [ ] User authentication (JWT)
- [ ] Environment variables for configuration
- [ ] Error handling middleware

#### AI Integration
- [ ] Integration with at least one AI API:
  - OpenAI (ChatGPT, DALL-E, Whisper)
  - Anthropic Claude
  - Hugging Face models
  - Google Gemini
  - Stability AI
  - Or other approved AI service
- [ ] Meaningful use of AI (not just a chatbot)
- [ ] Cost optimization strategies
- [ ] Rate limiting to prevent abuse

#### Deployment
- [ ] Frontend deployed (Vercel, Netlify, etc.)
- [ ] Backend deployed (Railway, Render, Fly.io, etc.)
- [ ] Database hosted (MongoDB Atlas, Neon, etc.)
- [ ] Environment variables properly configured
- [ ] HTTPS enabled
- [ ] Custom domain (optional bonus)

#### Code Quality
- [ ] Clean, readable code
- [ ] Proper file/folder structure
- [ ] Meaningful comments
- [ ] No hardcoded secrets
- [ ] Git repository with good commit history
- [ ] README with comprehensive documentation

## Project Ideas

### Tier 1: Recommended Complexity

#### 1. AI Content Generator
- Blog post generator with customizable tone/style
- Social media caption generator
- Email template generator
- Features: User accounts, saved generations, export options

#### 2. AI Image Studio
- Generate images with multiple AI models
- Edit and enhance existing images
- Create variations of uploaded images
- Features: Gallery, collections, sharing

#### 3. AI Learning Assistant
- Subject-specific tutor (math, coding, languages)
- Quiz generation from topics
- Explain concepts with examples
- Features: Progress tracking, history, difficulty levels

#### 4. AI Code Review Tool
- Upload code for AI analysis
- Get suggestions for improvements
- Security vulnerability detection
- Features: Multiple languages, comparison view

#### 5. AI Customer Support Bot
- Intelligent chatbot for specific domain
- Knowledge base integration
- Ticket creation for human escalation
- Features: Analytics dashboard, training interface

### Tier 2: Advanced (if you're feeling ambitious)

#### 6. AI Video/Audio Transcription Service
- Upload video/audio files
- AI transcription with Whisper API
- Summary generation
- Features: Timestamped transcripts, keyword extraction

#### 7. AI Data Visualization Tool
- Upload CSV/JSON data
- AI suggests best visualizations
- Natural language queries to data
- Features: Interactive charts, export options

#### 8. AI Writing Companion
- Long-form content writing assistance
- Outline generation
- Tone consistency checker
- Features: Document management, collaboration

### Tier 3: Custom Idea
- **Propose your own idea!**
- Must meet all technical requirements
- Requires instructor approval by Week 21

## Project Milestones

### Checkpoint 1: Proposal & Design (June 13)
**Deliverables**:
- [ ] Project proposal document (1-2 pages)
  - Problem statement
  - Target audience
  - Key features
  - Technology stack
  - AI integration plan
- [ ] Wireframes/mockups of main pages
- [ ] Database schema design
- [ ] API endpoint documentation
- [ ] Timeline with milestones

**Evaluation**: Pass/Fail (must be approved to continue)

### Checkpoint 2: MVP Demo (June 20)
**Deliverables**:
- [ ] Working MVP with core features
- [ ] User authentication functional
- [ ] AI integration working
- [ ] Deployed (can be staging)
- [ ] GitHub repository with README

**Evaluation**: 20% of capstone grade

### Final Submission (June 22)
**Deliverables**:
- [ ] Complete application
- [ ] Production deployment
- [ ] Comprehensive README
- [ ] Video demo (3-5 minutes)
- [ ] Presentation slides

**Evaluation**: 50% of capstone grade

### Final Presentation (June 20 or 23)
**Deliverables**:
- [ ] 10-minute live presentation
- [ ] Live demo of application
- [ ] Q&A session

**Evaluation**: 30% of capstone grade

## Technical Architecture

### Recommended Stack

```
Frontend:
- React.js + Vite
- React Router
- Axios/Fetch API
- TailwindCSS or MUI/Chakra UI
- React Hook Form
- React Query (optional)

Backend:
- Node.js + Express.js
- JWT authentication
- bcrypt for password hashing
- Multer (if file uploads)
- CORS
- dotenv

Database:
- MongoDB with Mongoose
- OR PostgreSQL with Prisma/Sequelize

AI Services:
- OpenAI SDK
- Anthropic SDK
- Or respective API client

Deployment:
- Frontend: Vercel/Netlify
- Backend: Railway/Render
- Database: MongoDB Atlas/Neon
```

### Project Structure

```
capstone-project/
├── client/                 # Frontend React app
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/      # API calls
│   │   ├── contexts/      # React contexts
│   │   ├── hooks/         # Custom hooks
│   │   ├── utils/
│   │   └── App.js
│   └── package.json
│
├── server/                # Backend Express app
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   ├── services/          # AI service integration
│   ├── utils/
│   ├── server.js
│   └── package.json
│
├── .gitignore
├── README.md
└── docs/
    ├── API_DOCUMENTATION.md
    ├── SETUP_GUIDE.md
    └── USER_GUIDE.md
```

## Evaluation Criteria

### Technical Implementation (40 points)
| Criterion | Points |
|-----------|--------|
| Frontend functionality | 10 |
| Backend functionality | 10 |
| AI integration quality | 10 |
| Database design | 5 |
| Code quality & organization | 5 |

### Features & User Experience (25 points)
| Criterion | Points |
|-----------|--------|
| Feature completeness | 10 |
| User interface design | 8 |
| Error handling & validation | 7 |

### Deployment & Documentation (20 points)
| Criterion | Points |
|-----------|--------|
| Successful deployment | 10 |
| README documentation | 5 |
| API documentation | 5 |

### Presentation (15 points)
| Criterion | Points |
|-----------|--------|
| Clarity and organization | 5 |
| Live demo execution | 5 |
| Q&A responses | 5 |

**Total**: 100 points (25% of course grade)

## Bonus Points (+5 each, max +20)

1. **Testing**: Unit tests or integration tests
2. **CI/CD**: GitHub Actions or similar
3. **Advanced Features**: Significantly beyond requirements
4. **Custom Domain**: Professional domain name
5. **Accessibility**: WCAG AA compliance
6. **Performance**: Lighthouse score 90+

## README Requirements

Your README.md must include:

```markdown
# Project Title

Brief description of what your app does

## Features
- List of main features

## Tech Stack
- Frontend: React, ...
- Backend: Node.js, Express, ...
- Database: MongoDB/PostgreSQL
- AI: OpenAI API, ...

## Screenshots
[Include 2-3 screenshots]

## Live Demo
- Frontend: [URL]
- Backend API: [URL]

## Setup Instructions

### Prerequisites
- Node.js v18+
- npm or yarn
- MongoDB/PostgreSQL

### Installation
1. Clone repository
2. Install dependencies
3. Set up environment variables
4. Run application

### Environment Variables
```
VITE_API_URL=...
DATABASE_URL=...
OPENAI_API_KEY=...
JWT_SECRET=...
```

## API Documentation
Link to API docs or brief overview

## Future Improvements
List of planned features

## Author
Your name and links

## License
MIT (or your choice)
```

## Presentation Format

### Presentation Structure (10 minutes)
1. **Introduction** (1 min)
   - Project name and purpose
   - Problem it solves

2. **Demo** (5 min)
   - Live walkthrough of key features
   - Show AI integration in action
   - Demonstrate user flow

3. **Technical Overview** (3 min)
   - Architecture diagram
   - Technology choices and why
   - AI implementation details
   - Challenges and solutions

4. **Q&A** (5 min)
   - Answer technical questions
   - Discuss design decisions

### Presentation Tips
- Practice your demo multiple times
- Have backup (video) in case of tech issues
- Prepare for common questions
- Show enthusiasm for your project!

## Common Pitfalls to Avoid

1. ❌ Starting too late (start immediately!)
2. ❌ Overscoping (start simple, add features iteratively)
3. ❌ Not testing AI integration early
4. ❌ Hardcoding API keys
5. ❌ Ignoring error handling
6. ❌ Poor commit messages/history
7. ❌ Not documenting setup process
8. ❌ Leaving console.log statements
9. ❌ Not testing on production environment
10. ❌ Skipping checkpoints

## Resources

### AI API Documentation
- [OpenAI API Docs](https://platform.openai.com/docs)
- [Anthropic Claude Docs](https://docs.anthropic.com/)
- [Hugging Face](https://huggingface.co/docs)

### Deployment Guides
- [Vercel Deployment](https://vercel.com/docs)
- [Railway Deployment](https://docs.railway.app/)
- [MongoDB Atlas Setup](https://www.mongodb.com/docs/atlas/)

### Code Quality
- [ESLint](https://eslint.org/)
- [Prettier](https://prettier.io/)

## Getting Help

- **Office Hours**: Extended during capstone period
- **Project Check-ins**: Weekly during development
- **Instructor Feedback**: Available on checkpoints
- **Peer Review**: Optional code review sessions

## Submission

### Final Submission Package
1. GitHub repository URL (must be public)
2. Live application URLs (frontend + backend)
3. Video demo link (YouTube, Loom, etc.)
4. Presentation slides (PDF or Google Slides link)

### Submit via:
[Submission platform link]

---

## Important Dates Reminder

- **June 6**: Kickoff, form teams (if group project)
- **June 13**: Checkpoint 1 due
- **June 20**: Checkpoint 2 due + Presentations (Group 1)
- **June 22**: Final submission deadline
- **June 23**: Presentations (Group 2)

---

This is your chance to showcase your skills and create something you can be proud to show employers. Take it seriously, start early, and don't hesitate to ask for help!

**Best of luck with your capstone project!**

*Project assigned: Week 21 | Due: Week 23*
