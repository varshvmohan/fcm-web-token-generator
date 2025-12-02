# FCM Web Token Generator

A lightweight tool for generating Firebase Cloud Messaging (FCM) Web Push tokens directly from the browser.  
Useful for testing notifications, verifying client setup, and debugging FCM implementations.

### 🚀 Features

- Generate FCM Web Push tokens instantly  
- Pure HTML + JavaScript (no frameworks, no build tools)  
- Uses Firebase Web SDK v10+  
- Includes service worker for background notification handling  
- Secure structure with placeholder Firebase config  

### 📦 How to Use

#### 1. Add your Firebase config  
    Open **index.html** and replace placeholders:
    ```js
    const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
    };
    ```

#### 2. Add your Web Push VAPID key  
    ```js
    const vapidKey = "YOUR_VAPID_KEY";
    ```

#### 3. Start a local server  
    Example commands:

    ```bash
    python3 -m http.server
    ```

    or

    ```bash
    npx serve .
    ```

#### 4. Generate the token  
Open the local URL → Click **Generate Token** → Token appears in the textarea.

### 📁 Project Structure

```
fcm-web-token-generator/
│
├── index.html                 # Main UI + Firebase logic
├── firebase-messaging-sw.js  # Service Worker for push handling
├── README.md
└── .gitignore
```

### ⓘ Disclaimer
- Replace Firebase credentials with your own. Do NOT use your production keys here.
- This project is intended for **development/testing** — not production.

### 📄 License

MIT License — free to use, modify, and share.

### ❤️ Contributing

PRs are welcome. This repo is intentionally simple — keep contributions minimal and focused.
