<div align="center">
  <img src="https://raw.githubusercontent.com/m-shahzaib5911/ShadowLink-/main/frontend/public/logo512.png" alt="ShadowLink Logo" width="150"/>
  <h1>🔒 ShadowLink</h1>
  <p><strong>A secure, ephemeral, and anonymous end-to-end encrypted messaging platform.</strong></p>
</div>

---

**ShadowLink** is a privacy-first web application designed for secure, anonymous communication. Built with a React frontend and a lightweight PHP backend, it leverages military-grade AES-GCM encryption in the browser to ensure your messages are never readable by the server. 

Rooms are ephemeral, messages auto-delete after expiration, and no persistent accounts are required. 

## ✨ Key Features

- 🔐 **Zero-Knowledge Architecture:** Messages are encrypted and decrypted directly in your browser. The server only sees ciphertext.
- 👤 **100% Anonymous:** No sign-ups, no accounts, and no personal data collection. Just create a room and share the password.
- ⏰ **Ephemeral Storage:** Rooms and messages automatically expire and are purged from the database after a set duration.
- 🛡️ **Hardened Backend:** Protected with UUID validations, payload size limits, rate limiting, and strict Content Security Policies (CSP).
- 🎨 **Cyberpunk Aesthetic:** A immersive, dark-terminal UI featuring customized CSS and React components.
- ⚡ **Polling Sync:** Lightweight frontend polling ensures near real-time message delivery without the overhead of maintaining WebSocket connections.

## 🛠️ Technology Stack

- **Frontend:** React, TypeScript, CSS (Terminal-styled UI)
- **Encryption:** Web Cryptography API (`AES-GCM`, `PBKDF2`)
- **Backend:** PHP 8+ API endpoints
- **Database:** MySQL / MariaDB (PDO)

## 🚀 Deployment & Setup

ShadowLink is built as a Decoupled Single Page Application (SPA).

### 1. Backend Setup
1. Upload the contents of the `deploy/` directory to your web server (e.g., Apache `htdocs` or Nginx `public_html`).
2. Update `deploy/api/config.php` with your MySQL database credentials.
3. Navigate to `https://your-domain.com/api/setup.php` in your browser once to automatically initialize the database tables (`rooms`, `users`, `messages`, `rate_limits`).
4. Ensure `.htaccess` is correctly placed to allow frontend routing and block access to sensitive config files.

### 2. Frontend Build
If you wish to modify the UI or logic:
```bash
cd frontend
npm install
npm start       # Start local development server
npm run build   # Generate production-ready files
```
Once built, copy the contents of `frontend/build/` into the `deploy/` directory on your live server.

## 🔒 Security Practices implemented
- **Salting:** Cryptographic salts are generated dynamically per room to protect against rainbow table attacks.
- **Strict Validations:** All API inputs (User IDs, Room IDs) are rigorously validated against strict UUID v4 RegEx patterns. 
- **HTML Sanitization:** Display names are sanitized to prevent XSS.
- **Rate-Limiting:** IP-based request throttling is enforced on the PHP backend to mitigate DDoS or brute-force attempts.

---

<div align="center">
  <i>Built with privacy and security in mind by Code_Hunter (m-shahzaib5911).</i>
</div>
