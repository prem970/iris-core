# 👁️ Iris Core

Iris is a personal AI agent operating within the OpenClaw ecosystem. This repository contains the core configuration and structural logic that defines Iris's behavior and operational environment.

## 🚀 Getting Started with OpenClaw & Local LLMs

OpenClaw is a powerful framework that allows you to run a highly capable AI agent on your own hardware. To get a setup like Iris's, follow these steps:

### 1. Install OpenClaw
First, install the OpenClaw CLI on your host machine:
```bash
npm install -g openclaw
```

### 2. Setup Local LLM (via Ollama)
Iris is powered by local models to ensure privacy and speed. The recommended way to run these is via **Ollama**:
1. **Install Ollama:** Download it from [ollama.com](https://ollama.com).
2. **Pull a Model:** For a balance of reasoning and speed, we recommend `gemma4`:
   ```bash
   ollama run gemma4:31b
   ```
3. **Configure OpenClaw:** Set your default model in the OpenClaw config to point to your Ollama instance.

### 3. Initialize the Gateway
Start the OpenClaw gateway to manage the connection between your LLM and your communication channels:
```bash
openclaw gateway start
```

---

## 📱 Connecting Iris via Telegram

To interact with Iris through Telegram, you need to link a Telegram bot to your OpenClaw instance:

1. **Create a Bot:**
   - Message [@BotFather](https://t.me/botfather) on Telegram.
   - Use `/newbot` to create a new bot and receive your **API Token**.

2. **Link to OpenClaw:**
   - Use the OpenClaw configuration tool or CLI to add the Telegram provider.
   - Input your Bot Token when prompted.

3. **Start Chatting:**
   - Find your new bot on Telegram and send a message.
   - Iris will wake up, initialize its identity from the workspace, and be ready for your commands.

## 🛠️ Core Files in this Repo
- `AGENTS.md`: General operational guidelines and behavioral rules.
- `TOOLS.md`: Local environment notes and device mappings.
- `.gitignore`: Ensures sensitive memory and API data are never leaked.
