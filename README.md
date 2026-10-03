# NoteFlow

A clean and lightweight note-taking app for writing, organizing, and managing tasks in one place. NoteFlow combines markdown note editing, personal task lists, and cloud-backed storage so your work stays synced and easy to access.

## Why NoteFlow?

Whether you are collecting ideas, writing project notes, or tracking daily tasks, NoteFlow helps you stay focused without the clutter of a heavy productivity tool. It focuses on:

- Simple note creation and organization
- Markdown-based writing with a distraction-free editor
- Task tracking with completed and incomplete items
- Firebase-powered login and secure personal storage
- Quick import/export for notes and markdown files
- Optional AI-powered backend support for enhanced writing workflows

## Features

- User authentication with email/password and Google sign-in
- Create notes and task lists from the same dashboard
- Markdown editor with rich formatting controls
- Search notes quickly by title
- Download notes as .txt, .md, or .pdf
- Import existing text files into the app
- Persistent storage for each user through Firebase Realtime Database
- Responsive layout for desktop and smaller screens
- Backend API endpoint for AI-assisted requests

## Tech Stack

### Frontend
- React
- Vite
- Tailwind CSS
- Material UI
- EasyMDE for markdown editing
- react-markdown

### Backend
- Express.js
- Node.js
- Hugging Face inference endpoint for AI requests

### Data & Auth
- Firebase Authentication
- Firebase Realtime Database

## Project Structure

```text
NoteFlow/
├── backend/
│   ├── Server.js
│   ├── package.json
│   └── package-lock.json
├── public/
├── src/
│   ├── components/
│   ├── context/
│   ├── pages/
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── index.html
├── package.json
├── vite.config.js
├── eslint.config.js
├── package-lock.json
└── README.md
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm
- A Firebase project
- Optional: a Hugging Face token if you plan to use the AI backend endpoint

### 1) Clone the repository

```bash
git clone https://github.com/SKTVDY/NoteFlow.git
cd NoteFlow
```

### 2) Install frontend dependencies

```bash
npm install
```

### 3) Install backend dependencies

```bash
cd backend
npm install
```

### 4) Configure Firebase

The app currently initializes Firebase directly in `src/context/Firebase.jsx`. Replace the existing config object with your own Firebase project settings.

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID"
};
```

### 5) Start the app

Run the frontend:

```bash
npm run dev
```

Run the backend in a separate terminal:

```bash
cd backend
npm start
```

The frontend will typically run on Vite's default local port, while the backend listens on port `5000`.

## Build for Production

```bash
npm run build
```

## Usage

1. Create an account or sign in with Google.
2. Create a new note or task list from the sidebar.
3. Write in markdown using the editor.
4. Save your work automatically to Firebase.
5. Search, open, edit, or delete saved notes anytime.
6. Export your work as text, markdown, or PDF.

## Notes on the Backend AI Endpoint

The Express backend exposes a `/gpt` route for AI-based requests. To use it in a real deployment, make sure your server configuration uses a valid token and secure environment management instead of hardcoded API credentials.

## Contributing

Contributions are welcome. If you would like to improve NoteFlow, feel free to:

- Open an issue for bugs or feature requests
- Submit a pull request with clear changes
- Improve documentation, UI, or performance

## License

This project is currently distributed without an explicit license file. If you plan to use it in production or share it publicly, confirm the licensing terms with the project owner before doing so.

## Acknowledgements

- Firebase for authentication and real-time data storage
- React ecosystem and Vite for a fast development experience
- EasyMDE for markdown editing
- Material UI for UI components and icons
