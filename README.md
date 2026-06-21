# ai-chatbot-platform
A full-stack AI conversational platform built on the MERN stack, integrating Google's Gemini API for context-aware, real-time data streaming and JWT for data isolation.

# Intelligent MERN Chatbot (Gemini API Integration)

### 📌 Project Status
> **Note:** I am currently working on the system design and database planning for this project. Active coding on the backend and frontend will resume right after my university semester exams.

---

## 🚀 Project Overview
I am developing a full-stack AI chatbot application using the MERN stack. My goal is to use Google’s Gemini API to handle smart, context-aware conversations. I plan to include smooth message history tracking, media uploads, and voice recognition as the project grows.

## 🛠️ Tech Stack I'm Using
* **Frontend:** React.js and Tailwind CSS (using React Context API for user sessions and dark mode)
* **Backend:** Node.js and Express.js (modular REST API routing)
* **Database:** MongoDB with Mongoose (to save chat history and sessions)
* **AI Engine:** Google Gemini API (focusing on system prompts and context management)

---

## 📐 Database & API Design

### 1. Database Collections (MongoDB)
To keep the app fast and prevent data from getting too messy, I am using a **referenced relationship model** instead of nesting everything:

* **Users:** Stores account details (`_id`, `username`, `email`, `passwordHash`, `createdAt`).
* **Chat Sessions:** Connects conversations to specific users for the sidebar (`_id`, `userId`, `title`, `updatedAt`).
* **Messages:** Stores each message inside a chat (`_id`, `sessionId`, `sender`, `textContext`, `mediaUrl`, `timestamp`).

### 2. API Routes Blueprint
* `POST /api/auth/register` & `POST /api/auth/login` — For secure user signup and login.
* `GET /api/chats` — To load previous chat titles into the sidebar.
* `POST /api/chats/:sessionId/message` — To take the user's text, stream it through the Gemini API, save it to MongoDB, and return the response.

---

## 🗺️ My Development Roadmap
- [x] **Phase 1:** Design the system architecture and database layout (Current Phase 🎯)
- [ ] **Phase 2:** Set up the Node/Express server, connect MongoDB, and add authentication.
- [ ] **Phase 3:** Build the frontend React interface and message display window.
- [ ] **Phase 4:** Connect the Gemini API and tune the prompts for the best responses.
- [ ] **Phase 5:** Add extra features like voice recognition and image attachments.
