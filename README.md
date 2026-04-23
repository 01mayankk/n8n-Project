# 📘 AI Notes Generator (GATE Prep)

An AI-powered web application that generates **structured GATE-level study notes** using **Google Gemini API + n8n automation**.

## 🌐 Live Demo
👉 https://ainotes-generator.netlify.app/

## ✨ Features

- 🧠 Generate **GATE-level notes**
- 📚 Covers topics like Heap, Stack, Graph, DP, etc.
- ⚡ Clean structured output:
  - Title
  - Introduction
  - Key Points
  - Explanation
  - Complexity
  - MCQs
  - Summary
- 🎯 Properly formatted MCQs
- 🌍 Works from browser (Netlify hosted UI)
- 🔄 Backend automation using n8n

## 🧰 Tech Stack
- Frontend: HTML, CSS, JavaScript
- Backend Automation: n8n (Docker)
- AI Model: Google Gemini 2.5 Flash
- Hosting: Netlify
- Tunnel: ngrok

## 🏗️ Architecture

![Workflow](assets/workflow.png)

## ⚙️ Setup Instructions

1. Run n8n (Docker)
   ```
   docker run -it --rm \
     -p 5678:5678 \
     n8nio/n8n
   ```

2. Start ngrok
   ```
   ngrok http 5678
   ```
   Copy the generated URL: `https://xxxxx.ngrok-free.dev`

3. Update Frontend
   Replace webhook URL in `index.html`:
   ```
   https://xxxxx.ngrok-free.dev/webhook/notes-generator
   ```

4. Activate Workflow
   Open n8n UI: http://localhost:5678
   Click Activate / Publish

5. Run App
   Open Netlify link OR local HTML
   Enter topic → Generate notes 🎉

## ⚠️ Important Notes
- ngrok must be running
- n8n container must be active
- ngrok URL changes on restart
- Use production webhook, not test

## 📌 Example Topics
- Stack
- Queue
- Heap
- Graph
- Dynamic Programming

## 🚀 Future Improvements
- 📥 Export notes as PDF
- 🎯 Interactive MCQ quiz
- 🌙 Dark/Light mode
- ⚡ Streaming responses
- 🔐 Deploy backend (remove ngrok)

## 👨‍💻 Author
Mayank Kumar

⭐ If you like this project, give it a ⭐ on GitHub!
