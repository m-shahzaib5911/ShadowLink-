<div align="center">
  <img src="https://raw.githubusercontent.com/m-shahzaib5911/ShadowLink-/main/frontend/public/logo512.png" alt="ShadowLink Logo" width="150"/>

  <h1>ShadowLink</h1>

  <p><strong>Secure. Anonymous. Ephemeral.</strong></p>
  <p>An end-to-end encrypted messaging platform with zero-knowledge architecture — built for those who take privacy seriously.</p>
</div>

---

## Overview

ShadowLink is a privacy-first web application engineered for secure, anonymous communication. Built on a React/TypeScript frontend and a hardened PHP backend, it employs military-grade **AES-GCM encryption** entirely within the browser — meaning the server never has access to plaintext messages.

No accounts. No logs. No traces.

---

## Features

| Feature | Description |
|---|---|
| 🔐 **Zero-Knowledge Architecture** | All encryption and decryption occurs client-side. The server handles only ciphertext — your messages are unreadable at the server level. |
| 👤 **Fully Anonymous** | No registration, no accounts, and no personal data collection. Generate a room, share the password, and communicate. |
| ⏰ **Ephemeral by Design** | Rooms and messages carry a configurable expiry. Upon expiration, all data is automatically purged from the database. |
| 🛡️ **Hardened Backend** | Enforces UUID v4 validation, payload size restrictions, IP-based rate limiting, and strict Content Security Policies (CSP). |
| ⚡ **Lightweight Polling** | Near real-time message delivery via efficient frontend polling — without the complexity of persistent WebSocket connections. |
| 🎨 **Terminal-Inspired UI** | An immersive dark-terminal interface built with custom React components and CSS. |

---

## Technology Stack

- **Frontend:** React, TypeScript, CSS
- **Encryption:** Web Cryptography API — `AES-GCM`, `PBKDF2`
- **Backend:** PHP 8+
- **Database:** MySQL / MariaDB (via PDO)

---

## Security Implementation

ShadowLink's security model is built around the principle that **the server should never be trusted** with sensitive data.

- **Client-Side Encryption:** Messages are encrypted before transmission using AES-GCM with keys derived via PBKDF2 and dynamic per-room cryptographic salts.
- **Input Validation:** All API inputs are validated against strict UUID v4 RegEx patterns to prevent injection or enumeration attacks.
- **XSS Prevention:** Display names and user inputs are sanitized before rendering.
- **Rate Limiting:** IP-based throttling on all PHP endpoints mitigates brute-force and DDoS attempts.
- **CSP Headers:** Strict Content Security Policies restrict unauthorized resource loading.

---

<div align="center">
  <sub>Built with a focus on privacy and security by <strong>Code_Hunter</strong> (<a href="https://github.com/m-shahzaib5911">m-shahzaib5911</a>).</sub>
</div>
