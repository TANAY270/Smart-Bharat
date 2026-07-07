# Smart Bharat - GenAI Civic Companion Platform

Smart Bharat is a premium, Generative AI-powered web platform designed to simplify everyday civic interactions, promote municipal transparency, support digital inclusion, and improve accessibility for all citizens.

---

## 🌟 Key Features

### 1. 💬 Sahayak AI Companion
*   **Dual-Mode Engine**: Connects to the **Google Gemini API** (`gemini-2.5-flash` or `gemini-2.5-pro`) for live response streams, or runs on a high-fidelity **Offline NLP Simulator** using matching local rules if no API key is provided.
*   **Multilingual Support**: Real-time language detection and translations between **English**, **Hindi**, and **Hinglish**.
*   **Speech Accessibility**:
    *   🎤 **Speech-to-Text (STT)**: Voice-input query box.
    *   🔊 **Text-to-Speech (TTS)**: Audibly reads back AI responses with mute toggles.

### 2. ⚠️ Public Grievance (Report an Issue)
*   **Interactive Ward Map**: Canvas-based municipal road maps. Pin locations to automatically capture `X, Y` coordinates.
*   **Auto-Location**: Simulated browser GPS coordinate detector.
*   **AI Auto-Categorizer**: Real-time keyword scanning automatically matches and selects categories (e.g., Streetlights, Potholes, Water Supply) based on the user's description.
*   **Official Receipts**: Stamped confirmation cards with printable and downloadable receipt text files.

### 3. 📂 Status Tracker & Action Simulator
*   **Log Timelines**: Track complaints from submission, to inspector allocation, through active site repair, to resolution.
*   **Officer Simulation**: Allows administrators or testers to simulate official updates, updating timelines and changing map coordinate colors.
*   **Satisfaction Audit**: Citizen ratings (1-5 stars) upon resolution. Rates of 1 or 2 stars activate an **Escalate Case** process, re-opening the file and assigning it to the Senior Commissioner Auditor Board.

### 4. 📄 Document Helper & verification Lab
*   **Checklist Compiler**: Renders mandatory checklist requirements and schedules for citizenship services (Aadhaar, PAN, Passport, Ration Card, Voter ID, Income Certificate).
*   **Verification Lab**: Drop dummy files (e.g. name a text file `aadhaar_card.pdf` or `photo.jpg`) and the app's heuristic parser checks it off the list.

### 5. ♿ Accessibility Toolbar
*   **Font Size Adjuster**: Interactive buttons (`A+`, `A`, `A-`) in the sidebar scale the text size up to 130% and down to 85% to help elderly or visually impaired citizens.
*   **Dark Mode**: Contrast-compliant slate layout with glassmorphic cards.

---

## 🛠️ Technology Stack
*   **Core Structure**: Semantic HTML5.
*   **Styling**: Vanilla CSS3 (custom HSL variables, responsive grids, and transitions).
*   **Logic**: ES6+ Javascript Modules.
*   **AI Integration**: `@google/generative-ai` SDK.
*   **Tooling**: Vite (hot module reloading, production bundling).

---

## 🚀 Setup & Installation

### Prerequisites
*   Node.js (v18 or higher recommended)
*   npm (v9 or higher)

### 1. Install Dependencies
```bash
npm install
```

### 2. Run Local Development Server
```bash
npm run dev
```
The server will start at **http://localhost:5173/**. You can open this URL in any modern web browser (including Brave, Chrome, Safari, or Edge).

### 3. Build for Production
```bash
npm run build
```
Generates a static web bundle inside the `/dist` directory.

### 4. Preview Production Build
```bash
npm run preview
```

---

## 📂 Project Structure
```text
Smart Bharat/
├── index.html        # Main SPA interface, layouts, and modals
├── styles.css        # Theme variables, responsive layouts, and keyframe animations
├── app.js            # Main application logic, SDK, state, and simulators
├── package.json      # Dependencies and dev server configurations
└── README.md         # Documentation
```

---

## 🔒 Security Note (Gemini API Integration)
This application supports client-side API requests to Google Gemini for prototyping and testing ease. For production environments, it is recommended to set up a proxy backend server (e.g., Node/Express) to handle API keys and securely sign requests.
