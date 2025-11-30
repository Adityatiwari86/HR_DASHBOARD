HR Dashboard

A full-stack HR Dashboard project built using React + TypeScript (Vite) on the frontend and a lightweight Node.js + Express + TypeScript backend.
Includes modular components, API services, and environment-based configuration.


---

🚀 Features

⚛ Modern React 19 + TypeScript

⚡ Vite-powered frontend for fast dev + optimized production builds

🟦 Node.js + Express backend (TypeScript)

🔌 API-ready architecture with services folder

🔐 Secure .env.local support for API keys (e.g., Gemini API)

📂 Clean project structure for scalability



---

🛠 Tech Stack

Frontend

React 19

TypeScript

Vite

JSX/TSX Components

Modular services


Backend

Node.js

Express

TypeScript

ts-node

nodemon



---

📦 Prerequisites

Before running locally, ensure you have:

Node.js v18+

npm v8+



---

🔑 Environment Variables

Create a .env.local file in the root (already included but empty):

GEMINI_API_KEY=your_api_key_here

> ⚠ Never upload real API keys to GitHub
.env.local should stay in .gitignore.




---

▶ Run the Project Locally

1. Install dependencies

npm install

2. Install backend dependencies

cd backend
npm install
cd ..

3. Start the frontend (Vite)

npm run dev

Visit the dev server (usually):

http://localhost:5173


---

🖥 Backend — Run & Development

The backend lives inside /backend.
You can run it using ts-node or nodemon.

Option A — Run using ts-node

npx ts-node backend/server.ts

Option B — Dev mode with nodemon (auto restart)

npx nodemon --watch backend --exec "npx ts-node" backend/server.ts

Option C — Build + run compiled JS (Production-like)

npx tsc -p backend/tsconfig.json
node backend/dist/server.js


---

📁 Project Structure

/
├─ backend/
│  ├─ server.ts           # Main Node/Express server
│  ├─ package.json
│  ├─ tsconfig.json
│  └─ dist/               # Compiled JS output (after build)
│
├─ components/
│  └─ Meeting.tsx         # Example component
│
├─ services/              # Frontend API + helpers
│
├─ types.ts               # Shared TypeScript types
├─ constants.ts           # Constants used across app
├─ App.tsx                # Main app component
├─ index.tsx              # Frontend entry point
├─ index.html
├─ vite.config.ts
├─ tsconfig.json
├─ package.json
└─ .env.local


---

📦 Build for Production (Frontend)

npm run build

Preview production build:

npm run preview

Deploy the /dist folder to:

Vercel

Netlify

GitHub Pages

Any static host


Backend can be deployed to:

Render

Railway

Fly.io

AWS / DigitalOcean / VPS



---

🔧 Suggested Scripts (Optional)

Add to backend/package.json

"scripts": {
  "dev": "nodemon --watch . --exec \"ts-node\" server.ts",
  "start": "node dist/server.js",
  "build": "tsc -p tsconfig.json"
}


---

❗ Troubleshooting

Frontend not loading?

Check port 5173

If API calls fail, update backend URL in services


CORS error

Enable CORS in backend (already included in dependencies)

Gemini API not working

Ensure GEMINI_API_KEY is set in .env.local


Backend ts-node errors

Run:

cd backend
npm install


---

🤝 Contributing

1. Fork this repository


2. Create a new branch


3. Commit changes


4. Open a Pull Request




---

📄 License

This project is released under the MIT License.


---
