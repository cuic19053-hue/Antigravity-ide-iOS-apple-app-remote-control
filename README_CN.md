# 📱 Antigravity IDE iOS Apple Remote Control

**专为 Antigravity IDE 打造的零延迟 iOS 移动端桥接工具**

Antigravity IDE iOS Apple Remote Control 是一个轻量级、零延迟的远程控制桥接工具，允许您直接从 iPhone 或 iPad 的 Safari 浏览器中，远程控制本地的 Antigravity IDE 和 AI 编程助手。

## 🌟 为什么选择这个远程控制工具？

传统的 AI 编程助手往往将您限制在电脑桌前。本工具打破了这层物理屏障，并针对 Apple 生态进行了专门优化。
1. **随时随地在 iPhone 上写代码**：躺在床上或者在通勤路上？只需拿出您的 iPhone，就可以直接向您的本地 Antigravity AI 发送指令来重构代码或开发新功能。
2. **真正的本地环境**：您并不是在和一个云端机器人聊天。您的 iPhone 会安全地连接到您的本地电脑，在您真实的本地工作区中执行命令。
3. **零延迟与流式输出**：采用了 Server-Sent Events (SSE) 和本地内网穿透技术，实现实时的打字机效果及零延迟的 Markdown 渲染，完美兼容 iOS Safari。
4. **语音输入支持**：原生支持 Web Speech API，允许您直接在浏览器中使用 Siri 听写功能，解放双手控制您的 IDE。

## 🚀 快速启动

1. **安装依赖（零依赖！）**
   本工具使用了纯粹的原生 Node.js，力求将上手门槛降到最低。
   
2. **启动服务**
   ```bash
   node server.js
   ```

3. **对外网暴露服务** (可选，用于远程访问)
   ```bash
   npm run tunnel
   ```
   这将会启动一个 Cloudflare tunnel 隧道，为您提供一个可以在世界上任何地方通过 iPhone 访问的安全公网 URL。

## ⚙️ 配置 (AGENTS.md)

远程控制的工作原理是将您的聊天消息直接写入到 IDE 活跃工作区的消息队列中。
请将提供的 `.agents/AGENTS.md` 规则包含在您的项目中，这样您的 IDE 就会知道如何通过 `push-msg.js` 脚本自动将执行结果与消息回复推送回您的手机端，且绕过必须在电脑端手动点击 UI 按钮的限制。

---

🌐 **[English Documentation (英文文档)](./README.md)**
