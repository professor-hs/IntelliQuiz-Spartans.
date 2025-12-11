📘 IntelliQuiz — AI-Powered Quiz Generator
Upload. Generate. Learn.

Transform any PDF, DOCX, or text paragraph into a high-quality quiz using Gemini AI.

🔥 About IntelliQuiz
IntelliQuiz is an AI-driven quiz generation platform that instantly converts study materials into meaningful multiple-choice questions.
Built for students, educators, and competitive exam aspirants who want quick assessments with zero manual effort.

Upload → Extract → Generate → Quiz Ready 

Core Features:
  1.Upload File / Paste Text
  2.AI-Generated MCQs (Gemini 1.5 Flash)
  3.Concept Extraction + Explanation Generation
  4.Real-time Quiz Rendering
  5.Animated UI (React + Framer Motion)
  6.Optional quiz saving (MongoDB)
  7.Responsive and clean interface

Tech Stack:
   1.Frontend
      React.js
      Tailwind CSS
      Framer Motion
   2.Backend
      Node.js + Express
      Gemini 1.5 Flash API
      pdf-parse, mammoth, docx libraries
      MongoDB (optional)
   3.AI
     Google Gemini 1.5 Flash
      Custom prompt engineering (MCQ generation + validation)

System Architecture:
          ┌────────────┐
          │   Frontend │
          │ React + FM │
          └─────┬──────┘
                │
                ▼
        ┌──────────────┐
        │   Backend     │
        │ Node + Express│
        └──────┬────────┘
               │
               ▼
      ┌─────────────────┐
      │  AI Pipeline    │
      │ Gemini 1.5 API  │
      └──────┬──────────┘
             │
             ▼
   ┌─────────────────────┐
   │ Quiz JSON Generator  │
   └─────────────────────┘

Repository Structure:
/src
   /backend
      /routes
      /controllers
      /ai
   /frontend
      /components
      /pages
/docs
/models
README.md
package.json
.env.example

Installation & Setup:
1. Clone the Repository
git clone https://github.com/your-username/intelliquiz.git
cd intelliquiz

2. Backend Setup
cd backend
npm install


Create .env file:
GEMINI_API_KEY=your_key
MONGO_URI=your_mongo_uri (optional)


Run backend:
npm start

3. Frontend Setup
cd frontend
npm install
npm run dev


API Endpoints:
Upload & Generate Quiz
POST /api/generate-quiz
Body: {
  "text": "content or extracted text"
}
Response:
{
  "questions": [
    {
      "question": "",
      "options": ["A", "B", "C", "D"],
      "answer": "",
      "explanation": ""
    }
  ]
}

File Upload:
POST /api/upload
FormData: file

AI Prompt Summary:
A specially engineered prompt is used to generate:
High-quality MCQs
Unique questions
Balanced difficulty
Explanation for each answer
JSON formatted output

Testing:
Run backend tests:
npm test


Roadmap:
 Backend architecture
 AI quiz generator
 Frontend integration
 User login & dashboard
 Difficulty-level selector
 Export quiz to PDF
 Deployed version



Frontend Developer

UI/UX Designer
