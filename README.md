# To-Do App + Notes App (React)

Minor Project 04, Web Development (Unlox Academy)
**Author:** Chirakala Sanjana

## Project Overview

Two productivity apps built with **React.js** in a single project. Use the tabs at the top to switch between them:

1. **To-Do App** to organize your daily tasks
2. **Notes App** to write, search and organize notes

Both apps save their data in the browser, so nothing is lost on refresh.

## Features Implemented

### To-Do App
- Add new tasks
- Mark tasks as completed (and back to pending)
- Edit existing tasks (text and due date)
- Delete tasks, or clear all completed tasks at once
- Task status shown as a **Completed / Pending** badge
- *Bonus:* filter by All / Pending / Completed (with counts)
- *Bonus:* due dates, with **overdue** highlighting
- *Bonus:* Local Storage integration
- Pending-task count shown in the browser tab title

### Notes App
- Create, edit and delete notes
- All notes shown in a responsive card grid, newest first
- *Bonus:* search by title or content
- *Bonus:* categories (General, Study, Personal, Work, Ideas) with category filter
- *Bonus:* created / edited timestamps
- *Bonus:* Local Storage integration

### Responsive design
Both apps adapt to mobile and desktop screens (CSS Grid, Flexbox and media queries).

## Technologies Used

- React 18 (functional components and hooks)
- Vite (build tool and dev server)
- JavaScript (ES6+)
- CSS3
- Git and GitHub

## React Concepts Demonstrated

| Concept | Where |
|---|---|
| Functional components, JSX | every file in `src/components` |
| Props (data and callback props) | `TodoList` → `TodoItem`, `NoteList` → `NoteCard`, etc. |
| `useState` | forms, filters, editing state |
| `useEffect` | `useLocalStorage` hook (saving), `TodoApp` (tab title) |
| Event handling | forms, checkboxes, filter chips, edit/delete buttons |
| Conditional rendering | edit mode vs view mode, empty states, overdue label |
| List rendering with `.map()` | task list, note grid, filter buttons |
| Component reusability | `EmptyState`, `TabNav`, `useLocalStorage` used by both apps; `NoteForm` handles create and edit |

## JavaScript Concepts Demonstrated

- **ES6+:** arrow functions, template literals, destructuring, spread operator, `let` / `const`
- **Array methods:** `map()`, `filter()`, `find()`
- **Object manipulation:** immutable updates such as `{ ...todo, completed: !todo.completed }`

## Project Structure

```
todo-notes-react/
├── index.html
├── package.json
├── vite.config.js
└── src/
    ├── main.jsx                  # entry file
    ├── App.jsx                   # tab switching between the two apps
    ├── App.css / index.css       # styles
    ├── assets/                   # (reserved for images)
    ├── hooks/
    │   └── useLocalStorage.js
    ├── utils/
    │   └── helpers.js
    └── components/
        ├── common/   (TabNav, EmptyState)
        ├── todo/     (TodoApp, TodoForm, TodoFilters, TodoList, TodoItem)
        └── notes/    (NotesApp, NoteForm, SearchBar, NoteList, NoteCard)
```

## Setup Instructions

You need [Node.js](https://nodejs.org/) 18 or newer.

```bash
# 1. Clone the repository
git clone https://github.com/sanjanachirakala-lab/todo-notes-react.git
cd todo-notes-react

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev
```

Open the address shown in the terminal (usually http://localhost:5173).

To create a production build: `npm run build` (output goes to `dist/`).

## Screenshots

*(Optional: add screenshots of both apps here.)*
