# DTP Expert AI (Frontend)

This is the responsive web interface for the **DTP Expert AI** agent. It provides a chat-based environment where users can upload raster images and request professional vector conversions or specific design fixes.

## ✨ Features
* **Chat Interface:** A clean, dark-mode UI mimicking professional design tools.
* **Google Auth:** Secure sign-in via Firebase Authentication.
* **Smart Image Handling:** Client-side image compression (max 1920px) before upload to save bandwidth.
* **🛡️ Secure Error Handling:** System errors are sanitized. If generation fails, the UI provides a user-friendly message without revealing the underlying API provider, Model ID, or backend logic.
* **Interactive Tools:**
    * **Task Selector:** Pre-defined DTP tasks (Full Color, B&W, etc.).
    * **Fix Mode:** Context-aware "Fix" menus to correct specific AI errors.
    * **Zoom Viewer:** Click any image to inspect details.

## 🛠 Tech Stack
* **Core:** HTML5, CSS3 (Variables & Flexbox), Vanilla JavaScript.
* **Hosting:** Firebase Hosting.
* **Auth:** Firebase Authentication (Google Provider).
* **Backend:** Connects to the [DTP Expert Backend](https://github.com/ViThaDev/dtp-genai-backend).

## 🚀 Setup & Configuration
This project requires a Firebase project and a deployed backend.

1.  **Clone the repository.**
2.  **Configure `index.html`:**
    Open `index.html` and replace the placeholder values with your actual Firebase credentials:
    ```javascript
    const firebaseConfig = {
        apiKey: "YOUR_API_KEY",
        authDomain: "YOUR_PROJECT.firebaseapp.com",
        // ... other config
    };
    
    const FUNCTION_URL = "YOUR_CLOUD_FUNCTION_URL";
    ```
3.  **Deploy:**
    ```bash
    firebase deploy
    ```
