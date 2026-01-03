Skills Management System - Frontend

This is the frontend application for the Skills Management System, built using React and Tailwind CSS. It allows users to manage personnel, skills, and projects, and integrates seamlessly with the backend API.

Table of Contents

Features

Tech Stack

Prerequisites

Installation

Environment Variables

Available Scripts

Folder Structure

Testing

API Integration

Contributing

License

Features

View, create, update, and delete personnel.

Assign skills to personnel with proficiency levels.

View, create, update, and delete skills.

View, create, update, and delete projects.

Assign required skills to projects with minimum proficiency.

Responsive UI built with Tailwind CSS.

Easy integration with backend API for real-time data.

Tech Stack

React.js (v18+)

React Router for routing

Tailwind CSS for styling

Axios for API requests

React Icons / Lucide-React for UI icons

Vite as build tool

Prerequisites

Node.js installed (Download Node.js
)

Backend API running and accessible (default: http://localhost:5000)

Package manager: npm or yarn

Installation

Clone the repository:

git clone <your-frontend-repo-url>
cd SRMfrontend


Install dependencies:

npm install


Start the development server:

npm run dev


The app will run at http://localhost:5173 (default Vite port).

Make sure your backend API is running and accessible at the configured URL.

Environment Variables

Create a .env file in the root directory:

VITE_API_BASE_URL=http://localhost:5000/api


VITE_API_BASE_URL should point to your backend API.

All API calls use this base URL.

Available Scripts
Command	Description
npm run dev	Start development server
npm run build	Build the production-ready app
npm run preview	Preview the production build locally
Folder Structure
SRMfrontend/
├─ src/
│  ├─ components/     # Reusable UI components
│  ├─ pages/          # Pages for routing
│  ├─ api/            # Axios API configurations and services
│  ├─ routes/         # React Router routes
│  ├─ utils/          # Utility functions
│  ├─ App.jsx
│  └─ main.jsx
├─ public/            # Static assets
├─ .env               # Environment variables
├─ package.json
└─ vite.config.js

Testing

Use the app in your browser and interact with the UI.

Test personnel, skills, and project CRUD operations.

Use developer tools to monitor API calls and ensure they hit the correct endpoints.

Optional: Use Postman to test backend independently before testing frontend integration.

API Integration

Base URL: VITE_API_BASE_URL

Personnel endpoints: /personnel

Skills endpoints: /skills

Projects endpoints: /projects

Example: Fetch all personnel:

import axios from 'axios';

const API_BASE = import.meta.env.VITE_API_BASE_URL;

export const getAllPersonnel = async () => {
    const response = await axios.get(`${API_BASE}/personnel`);
    return response.data;
};


Example: Assign skill to personnel:

axios.post(`${API_BASE}/personnel/1/skills`, {
    skill_id: 3,
    proficiency: "Advanced"
});

Contributing

Fork the repository.

Create a branch: git checkout -b feature/your-feature.

Make your changes.

Commit changes: git commit -m "Add new feature".

Push to branch: git push origin feature/your-feature.

Open a pull request.

License

MIT License © 2026
