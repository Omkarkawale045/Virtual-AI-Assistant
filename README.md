# AI-Assistant

# 🚀 Installation & Setup Guide

Follow the steps below to run this project locally.

# 📌 Prerequisites

Before installing, ensure you have:

🟢 Node.js (LTS) — Download from NodeJS official site

🗄️ MongoDB Atlas Account

🔐 Required API Keys (explained below)

📂 Step 1 — Clone the Repository
```
git clone https://github.com/Omkarkawale045/Virtual-AI-Assistant.git
cd Virtual-AI-Assistant
```
# ⚙️ Step 2 — Configure Backend (Server)

Open the backend in terminal:
```
cd backend
```

Install backend dependencies:
```
npm install
```
# 🔐 Create .env File in /backend

Create a file named .env and add the following structure:
```
MONGO_URI=your_mongo_atlas_connection_string
JWT_SECRET=your_jwt_secret_key
OPENAI_API_KEY=your_openai_key
CLOUDINARY_NAME=your_name
CLOUDINARY_API_KEY=your_key
CLOUDINARY_SECRET=your_secret
```

⚠️ Do NOT push .env file to GitHub.
Add it to .gitignore.

# 🗄️ Step 2.1 — Setup MongoDB Atlas
```
Visit: https://www.mongodb.com/cloud/atlas
```
Create a free cluster

Create a user (username & password)

Whitelist IP: 0.0.0.0/0

Click → Connect

Select → MongoDB Driver

Copy connection string and replace <password> with your DB password.

✔️ Paste it inside .env under MONGO_URI.

# 🔐 Step 2.2 — Generate & Add API Keys

Depending on features used:
```
Service	Purpose	Link
OpenAI	AI assistant response	https://platform.openai.com

Cloudinary	File/media storage	https://cloudinary.com

JWT Secret	Authentication/session	Generate random secret string

Generate JWT secret using:

node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"
```
# ▶️ Run Backend
```
npm run dev
```

Backend runs on: http://localhost:5000

# 🎨 Step 3 — Setup & Run Frontend

Open a new terminal:
```
cd frontend
npm install
npm run dev
```

Frontend runs on: http://localhost:5173

# 🔧 Step 4 — (Optional) Admin Panel Setup

If the project includes an admin panel:
```
cd admin
npm install
npm run dev
```

Admin UI: http://localhost:5174

# ☑️ Final Checklist
Requirement	Status
Backend running	✔
Frontend running	✔
MongoDB connected	✔
API keys configured	✔
No errors in terminal	✔
🎯 You’re Ready!

Your Virtual AI Assistant is now fully running with:

🧠 AI Processing

🗄️ Database Storage

☁ Cloud Storage

🔐 Secure Authentication

# 🛡 Security Reminder

Never upload:

.env

Mongo URI

API Keys

Tokens

Add this to .gitignore:
```
.env
/node_modules
```
