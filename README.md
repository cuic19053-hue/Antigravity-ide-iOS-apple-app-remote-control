# 📱 Pocket-IDE (Agent Remote Link)

**Zero-latency Mobile IDE Bridge for AI Agents**

Pocket-IDE is a lightweight, zero-latency bridge that allows you to control your local IDE and AI agents (like Cursor, Windsurf, or Antigravity) directly from your mobile phone's browser.

## 🌟 Why Pocket-IDE?

Traditional AI coding assistants lock you to your desktop. Pocket-IDE breaks that physical barrier.
1. **Code From Anywhere**: Lying in bed or on the commute? Pull out your phone and command your local AI to refactor code.
2. **True Local Environment**: You are not talking to a cloud bot. Your phone connects securely to your local machine, executing commands in your real workspace.
3. **Zero Latency & Streaming**: Uses Server-Sent Events (SSE) and local tunneling to achieve instant typing indicators and zero-latency markdown rendering.

## 🚀 Quick Start

1. **Install dependencies (none!)**
   Pocket-IDE uses pure vanilla Node.js to minimize friction.
   
2. **Start the server**
   ```bash
   npm start
   ```

3. **Expose to the Internet** (Optional, for remote access)
   ```bash
   npm run tunnel
   ```
   This will start a Cloudflare tunnel and give you a secure public URL you can open on your iPhone/Android.

## ⚙️ Configuration (AGENTS.md)

Pocket-IDE works by writing messages directly into the IDE's active workspace.
Include the provided `.agents/AGENTS.md` in your project so your IDE knows how to reply back to the mobile client using `push-msg.js`.
