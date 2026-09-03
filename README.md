# 📱 Antigravity IDE iOS Apple Remote Control

🌐 **[中文文档 (Chinese README)](./README_CN.md)**

**Zero-latency iOS Mobile Bridge for Antigravity IDE**

Antigravity IDE iOS Apple Remote Control is a lightweight, zero-latency bridge that allows you to control your local Antigravity IDE and AI agents directly from your iPhone or iPad browser (Safari).

## 🌟 Why this Remote Control?

Traditional AI coding assistants lock you to your desktop. This tool breaks that physical barrier, specifically optimized for the Apple ecosystem.
1. **Code From Anywhere on your iPhone**: Lying in bed or on the commute? Pull out your iPhone and command your local Antigravity AI to refactor code or write new features.
2. **True Local Environment**: You are not talking to a cloud bot. Your iPhone connects securely to your local machine, executing commands in your real workspace.
3. **Zero Latency & Streaming**: Uses Server-Sent Events (SSE) and local tunneling to achieve instant typing indicators and zero-latency markdown rendering perfectly compatible with iOS Safari.
4. **Voice Input Support**: Native support for Web Speech API, allowing you to use Siri Dictation directly in the browser to control your IDE hands-free.

## 🚀 Quick Start

1. **Install dependencies (none!)**
   This tool uses pure vanilla Node.js to minimize friction.
   
2. **Start the server**
   ```bash
   node server.js
   ```

3. **Expose to the Internet** (Optional, for remote access)
   ```bash
   npm run tunnel
   ```
   This will start a Cloudflare tunnel and give you a secure public URL you can open on your iPhone anywhere in the world.

## ⚙️ Configuration (AGENTS.md)

The remote control works by writing messages directly into the IDE's active workspace message queue.
Include the provided `.agents/AGENTS.md` rules in your project so your IDE knows how to automatically reply back to the mobile client using `push-msg.js` and bypasses manual UI clicks.

