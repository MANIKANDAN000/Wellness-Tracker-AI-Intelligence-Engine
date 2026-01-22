# 🌿 Elite Wellness Tracker & AI Intelligence Engine

Welcome to the **Elite Wellness Tracker**, a next-generation health management platform powered by a hyper-personalized, real-time AI Assistant. This project transforms standard wellness monitoring into an immersive, data-driven coaching experience.

---

## ✨ Project Highlights

- 🔐 Role-Based Authentication (Admin & Candidate)
- 🤖 Elite AI Wellness Assistant (GPT-powered)
- 🧠 Context-Aware Responses (BMI, steps, hydration)
- 🌸 Women-Centric Wellness Logic (Menstrual cycle based advice)
- 🎭 AI Persona Switching (Coach / Scientist / Zen)
- 🎥 Embedded Workout & Diet Videos
- 🖼️ Visual Learning with Images
- 💎 Glassmorphism UI & Modern Animations

## 🚀 Key "Elite AI" Features

The flagship feature of this application is the **Elite AI Wellness Assistant**, designed to feel like a high-end personal consultant.

### 1. Real-Time Conversational Intelligence
- **Persistent Context**: Unlike standard bots, this assistant remembers your previous questions in the same session, allowing for complex follow-up queries.
- **GPT-4o-Mini Engine**: Powered by the state-of-the-art `gpt-4o-mini` model for superior accuracy and medically sound wellness explanations.

### 2. Hyper-Personalization (Data-Aware)
- **Zero-Input Context**: The AI automatically fetches your latest **BMI**, **Hydration levels**, and **Step counts** from the database to give advice that is "surgically precise."
- **Hormonal Bio-Sync**: For female users, the AI detects the current menstrual phase (Menstrual, Follicular, Ovulatory, Luteal) and adapts its nutrition and exercise advice accordingly.

### 3. Multimedia Wellness Encyclopedia
- **Embedded Video Coaching**: Asking for exercises or recipes triggers the AI to find and embed **playable YouTube videos** directly in your chat bubble.
- **Visual Learning**: Every response is accompanied by a gallery of high-resolution Unsplash images to illustrate the concepts.

### 4. Persona Selection
Switch between three distinct AI personalities in real-time:
- **⚡ Coach**: High energy, motivational, and action-oriented.
- **🔬 Scientist**: Data-driven, analytical, and focused on biological mechanisms.
- **🍃 Zen**: Mindful, calm, and focused on holistic balance and stress relief.


ADMIN LOGIN
USERNAME: admin
PASSWORD: admin123
---

## 🛠️ Technical Architecture

### Core Tech Stack
- **Backend**: Python 3.x, Flask (Web Framework)
- **Database**: SQLAlchemy ORM (SQL Database)
- **AI Engine**: OpenAI API (GPT-4o-mini)
- **Frontend**: Jinja2 Templates, Vanilla CSS (Glassmorphism), Vanilla JavaScript


## 🧠 Elite AI Assistant Capabilities

- Remembers previous messages during the session
- Automatically reads wellness data from database
- Adjusts advice based on gender & hormonal phase
- Supports real-time persona switching
- Embeds YouTube workout & diet videos
- Displays visual image galleries for clarity

---

## 🔐 How to Get OpenAI API Key

1. Visit: https://platform.openai.com  
2. Login / Sign up  
3. Go to Dashboard → API Keys  
4. Click "Create new secret key"  
5. Copy the generated key  

Example:
sk-xxxxxxxxxxxxxxxxxxxx

---

## ⚙️ API Key Setup

Option 1: Direct method (Simple)

Edit `config.py`:
```python
OPENAI_API_KEY = "your_openai_api_key_here"

---

## 🏃 How to Run the Application

### 1. Prerequisites
- Python 3.8+ installed.
- A valid **OpenAI API Key**.

### 2. Installation
Clone the repository and install dependencies:
```bash
pip install -r requirements.txt
```

### 3. Configuration
Open `config.py` and add your OpenAI API Key:
```python
OPENAI_API_KEY = "your_actual_key_here"
```

### 4. Launch
Start the development server:
```bash
python app.py
```
Visit `http://127.0.0.1:5000` in your browser.

---

## 📖 How to Read the Code

To understand how the **Elite AI** works, follow this flow:

1.  **Context Ingestion (`routes/ai_assistant.py`)**: Look at the `query()` function. Notice how it queries `WellnessData.query` and `MenstruationLog.query` before even talking to the AI.
2.  **Prompt Engineering**: Inside `ai_assistant.py`, examine the `context` string. This is where we instruct the AI to use specific formats, embed videos, and use the user's live data.
3.  **Frontend Rendering (`templates/ai/chat.html`)**: Check the `formatResponse()` JS function. This uses Regex to turn markdown images into beautiful UI elements and YouTube links into recursive iframes.
4.  **State Management**: See how `messageHistory = []` in the JS keeps track of the conversation and sends it back to the Python server in every request.

---

🔄 Application Flow

Landing Page
→ Login / Register
→ Role-Based Dashboard
→ Wellness Data Fetch
→ Elite AI Prompt Creation
→ OpenAI Response
→ Video + Image Rendering

🧪 AI Logic Flow

User Question
→ Fetch Wellness Data
→ Build Context Prompt
→ OpenAI API Call
→ AI Response
→ UI Rendering

🛑 Common Issues & Fixes

pip not recognized:

Ensure Python is added to PATH

Run: python -m ensurepip --upgrade

API key error:

Verify API key

Restart terminal after setting environment variable

Module not found:

Activate virtual environment

Reinstall requirements

🚀 Future Enhancements

Mobile App Integration

Advanced Analytics Dashboard

Payment Gateway Integration

Cloud Deployment (AWS / Render)

Emotion-Aware AI Coaching

👨‍💻 Developed By

Manikandan Ravikumar
MCA | Python Developer | AI Engineer
Madurai, Tamil Nadu
