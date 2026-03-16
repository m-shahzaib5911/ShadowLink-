<div align="center">
  <h1>ShadowLink</h1>

  <p><em>Secure. Anonymous. Ephemeral. Leave No Trace.</em></p>

  ![last commit](https://img.shields.io/github/last-commit/m-shahzaib5911/ShadowLink-)
  ![languages](https://img.shields.io/github/languages/count/m-shahzaib5911/ShadowLink-)
  ![top language](https://img.shields.io/github/languages/top/m-shahzaib5911/ShadowLink-)
  ![license](https://img.shields.io/github/license/m-shahzaib5911/ShadowLink-)

  <br/>

  **Built with the tools and technologies:**

  ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
  ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
  ![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
  ![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)

</div>

---

> **ShadowLink** — Because some conversations were never meant to be stored.
>
> *For personal privacy and authorized use only.*

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
