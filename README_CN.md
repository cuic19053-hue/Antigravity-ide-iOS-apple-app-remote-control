# 📱 Pocket-IDE (智能体远程连接)

**专为 AI 智能体打造的零延迟移动端 IDE 桥接工具**

Pocket-IDE 是一个轻量级、零延迟的桥接工具，允许您直接从手机浏览器的网页端，远程控制本地 IDE 和 AI 编程助手（如 Cursor、Windsurf 或 Antigravity）。

## 🌟 为什么选择 Pocket-IDE？

传统的 AI 编程助手往往将您限制在电脑桌前。Pocket-IDE 打破了这层物理屏障。
1. **随时随地写代码**：躺在床上或者在通勤路上？只需拿出手机，就可以直接向您的本地 AI 发送指令来重构代码。
2. **真正的本地环境**：您并不是在和一个云端机器人聊天。您的手机会安全地连接到您的本地电脑，在您真实的本地工作区中执行命令。
3. **零延迟与流式输出**：采用了 Server-Sent Events (SSE) 和本地内网穿透技术，实现实时的打字机效果及零延迟的 Markdown 渲染。

## 🚀 快速启动

1. **安装依赖（零依赖！）**
   Pocket-IDE 使用了纯粹的原生 Node.js，力求将上手门槛降到最低。
   
2. **启动服务**
   ```bash
   npm start
   ```

3. **对外网暴露服务** (可选，用于远程访问)
   ```bash
   npm run tunnel
   ```
   这将会启动一个 Cloudflare tunnel 隧道，为您提供一个可以在 iPhone 或 Android 手机上打开的安全公网 URL。

## ⚙️ 配置 (AGENTS.md)

Pocket-IDE 的工作原理是将您的聊天消息直接写入到 IDE 活跃工作区的文件系统中。
请将提供的 `.agents/AGENTS.md` 文件包含在您的项目中，这样您的 IDE 智能体就会知道如何通过 `push-msg.js` 脚本将执行结果与消息回复推送回您的手机端。
