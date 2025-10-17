# Mini Project 02: Todo List Application

## Project Overview

Build an interactive todo list application using HTML, CSS, and JavaScript (with React). This project will help you understand state management, event handling, and creating dynamic user interfaces.

## Due Date
**Week 8** - March 13, 2025

## Learning Objectives

- Build a React application from scratch
- Manage component state with hooks
- Handle user input and events
- Implement CRUD operations (Create, Read, Update, Delete)
- Use localStorage for data persistence
- Apply conditional rendering
- Style React components

## Project Requirements

### Core Features (Required)

#### 1. Add Todos
- [ ] Input field to enter new todo
- [ ] Button to add todo to list
- [ ] Clear input after adding
- [ ] Prevent empty todos

#### 2. Display Todos
- [ ] Show list of all todos
- [ ] Display todo text
- [ ] Show completion status
- [ ] Show creation date/time (optional)

#### 3. Mark as Complete
- [ ] Checkbox to toggle completion
- [ ] Visual indication of completed todos
- [ ] Strike-through or different styling

#### 4. Delete Todos
- [ ] Delete button for each todo
- [ ] Confirmation before delete (optional)
- [ ] Remove from list immediately

#### 5. Filter Todos
- [ ] Show all todos
- [ ] Show only active (incomplete) todos
- [ ] Show only completed todos
- [ ] Filter buttons/tabs

#### 6. Todo Count
- [ ] Display total number of todos
- [ ] Display number of active todos
- [ ] Display number of completed todos

### Technical Requirements

#### React Components
- [ ] App component (main container)
- [ ] TodoForm component (input and add button)
- [ ] TodoList component (list container)
- [ ] TodoItem component (individual todo)
- [ ] Filter component (filter buttons)

#### State Management
- [ ] Use useState for todo list
- [ ] Use useState for filter state
- [ ] Use useState for input value
- [ ] Proper state updates (immutability)

#### Functionality
- [ ] Add new todos
- [ ] Toggle todo completion
- [ ] Delete todos
- [ ] Filter todos by status
- [ ] Data persists on page refresh (localStorage)

#### Styling
- [ ] Clean, modern design
- [ ] Responsive layout
- [ ] Hover effects
- [ ] Visual feedback for interactions
- [ ] Different styles for completed todos

## Bonus Features (+5 points each)

1. **Edit Todos**: Double-click to edit existing todo text
2. **Priority Levels**: Add priority (low, medium, high) with color coding
3. **Due Dates**: Add due date to todos with date picker
4. **Categories**: Organize todos by categories/tags
5. **Search**: Search/filter todos by text
6. **Clear Completed**: Button to remove all completed todos
7. **Dark Mode**: Toggle between light and dark themes
8. **Drag and Drop**: Reorder todos by dragging
9. **Statistics**: Show productivity stats and charts

## Recommended Project Structure

```
todo-app/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── App.js
│   │   ├── TodoForm.js
│   │   ├── TodoList.js
│   │   ├── TodoItem.js
│   │   └── FilterButtons.js
│   ├── styles/
│   │   ├── App.css
│   │   ├── TodoForm.css
│   │   ├── TodoList.css
│   │   └── TodoItem.css
│   ├── utils/
│   │   └── localStorage.js
│   ├── index.js
│   └── index.css
├── package.json
└── README.md
```

## Component Structure Example

### App.js (Main Component)
```javascript
import { useState, useEffect } from 'react';
import TodoForm from './components/TodoForm';
import TodoList from './components/TodoList';
import FilterButtons from './components/FilterButtons';

function App() {
  const [todos, setTodos] = useState([]);
  const [filter, setFilter] = useState('all');

  // Load from localStorage
  useEffect(() => {
    const savedTodos = localStorage.getItem('todos');
    if (savedTodos) {
      setTodos(JSON.parse(savedTodos));
    }
  }, []);

  // Save to localStorage
  useEffect(() => {
    localStorage.setItem('todos', JSON.stringify(todos));
  }, [todos]);

  // Add more functions...

  return (
    <div className="app">
      <h1>My Todo List</h1>
      <TodoForm onAdd={addTodo} />
      <FilterButtons filter={filter} setFilter={setFilter} />
      <TodoList todos={filteredTodos} onToggle={toggleTodo} onDelete={deleteTodo} />
    </div>
  );
}
```

### TodoItem.js (Individual Todo)
```javascript
function TodoItem({ todo, onToggle, onDelete }) {
  return (
    <div className={`todo-item ${todo.completed ? 'completed' : ''}`}>
      <input
        type="checkbox"
        checked={todo.completed}
        onChange={() => onToggle(todo.id)}
      />
      <span>{todo.text}</span>
      <button onClick={() => onDelete(todo.id)}>Delete</button>
    </div>
  );
}
```

## Data Structure

### Todo Object
```javascript
{
  id: 1, // or use UUID
  text: "Complete React project",
  completed: false,
  createdAt: "2025-01-20T10:30:00",
  // Optional bonus fields:
  priority: "high",
  dueDate: "2025-01-25",
  category: "work"
}
```

## Styling Suggestions

### Color Scheme
```css
:root {
  --primary-color: #4a90e2;
  --secondary-color: #f39c12;
  --success-color: #27ae60;
  --danger-color: #e74c3c;
  --text-color: #2c3e50;
  --bg-color: #ecf0f1;
  --card-bg: #ffffff;
  --border-color: #bdc3c7;
}
```

### Example Styles
```css
.todo-item {
  display: flex;
  align-items: center;
  padding: 1rem;
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  margin-bottom: 0.5rem;
}

.todo-item.completed {
  opacity: 0.6;
}

.todo-item.completed span {
  text-decoration: line-through;
  color: #95a5a6;
}
```

## Evaluation Criteria

| Category | Points | Description |
|----------|--------|-------------|
| Core Functionality | 30 | All required features work |
| React Best Practices | 20 | Proper component structure, hooks usage |
| State Management | 15 | Correct state updates, data flow |
| localStorage | 10 | Data persists correctly |
| UI/UX Design | 15 | Clean, intuitive interface |
| Code Quality | 10 | Clean, readable, commented code |
| **Total** | **100** | |

## Getting Started

### Step 1: Setup (30 minutes)
```bash
# Create React app
npx create-react-app todo-app
cd todo-app

# Start development server
npm start
```

### Step 2: Plan Components (30 minutes)
- Sketch component hierarchy
- Define props and state
- Plan data flow

### Step 3: Build Core Features (4-5 hours)
- Create components
- Implement add functionality
- Implement toggle and delete
- Add filtering

### Step 4: Add localStorage (1 hour)
- Save todos on change
- Load todos on mount
- Handle edge cases

### Step 5: Styling (2-3 hours)
- Create CSS files
- Style components
- Make responsive
- Add animations

### Step 6: Testing & Debugging (1-2 hours)
- Test all features
- Fix bugs
- Test on different browsers
- Test on mobile

## Common Pitfalls to Avoid

1. ❌ Mutating state directly (use spread operator or map)
2. ❌ Not using keys in lists
3. ❌ Forgetting to handle edge cases (empty list, empty input)
4. ❌ Not saving to localStorage
5. ❌ Poor component organization
6. ❌ Inline styles everywhere (use CSS files)
7. ❌ Not testing filter functionality
8. ❌ Complicated state management

## Testing Checklist

- [ ] Can add new todos
- [ ] Can toggle todo completion
- [ ] Can delete todos
- [ ] Filters work correctly (all, active, completed)
- [ ] Todo count is accurate
- [ ] Data persists after page refresh
- [ ] Can't add empty todos
- [ ] Works on mobile devices
- [ ] No console errors
- [ ] Responsive on all screen sizes

## Submission Requirements

### GitHub Repository
1. Initialize git in project folder
2. Create repository: `react-todo-app`
3. Push all code
4. Include README with:
   - Project description
   - Features list
   - Screenshots
   - How to run locally

### Deployment
Deploy to one of:
- [Vercel](https://vercel.com/) (recommended for React)
- [Netlify](https://www.netlify.com/)
- [GitHub Pages](https://pages.github.com/)

### Submission Checklist
- [ ] GitHub repository URL
- [ ] Live demo URL
- [ ] All features working
- [ ] README with setup instructions
- [ ] Clean code (no commented-out code)
- [ ] No console errors

## Resources

### React Documentation
- [React Hooks](https://react.dev/reference/react)
- [useState Hook](https://react.dev/reference/react/useState)
- [useEffect Hook](https://react.dev/reference/react/useEffect)

### Tutorials
- [React Todo List Tutorial](https://www.freecodecamp.org/news/how-to-build-a-todo-list-with-react-hooks/)
- [localStorage in React](https://blog.logrocket.com/using-localstorage-react-hooks/)

### Tools
- [UUID Generator](https://www.npmjs.com/package/uuid) - For unique IDs
- [date-fns](https://date-fns.org/) - Date formatting
- [React Icons](https://react-icons.github.io/react-icons/) - Icon library

## Example Implementations (for inspiration only)

- [TodoMVC](https://todomvc.com/)
- [Microsoft To Do](https://to-do.microsoft.com/)
- [Todoist](https://todoist.com/)

## Advanced Tips

### Using Custom Hooks
```javascript
// useLocalStorage.js
function useLocalStorage(key, initialValue) {
  const [value, setValue] = useState(() => {
    const saved = localStorage.getItem(key);
    return saved ? JSON.parse(saved) : initialValue;
  });

  useEffect(() => {
    localStorage.setItem(key, JSON.stringify(value));
  }, [key, value]);

  return [value, setValue];
}
```

### Generating Unique IDs
```javascript
// Simple approach
const id = Date.now();

// Better approach (install uuid)
import { v4 as uuidv4 } from 'uuid';
const id = uuidv4();
```

## Getting Help

- **Office Hours**: Wednesdays, 5:00-6:00 PM
- **Discussion Forum**: [Link]
- **React Documentation**: [https://react.dev](https://react.dev)

---

This project is a fundamental exercise in React development. Focus on understanding state management and component composition. These concepts will be crucial for all future React projects!

**Good luck!**

*Project assigned: Week 5 | Due: Week 8*
