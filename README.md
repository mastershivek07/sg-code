<div align="center">

# ⚡ SG CODE

### AI-Powered Coding Assistant — Native Desktop Terminal

**Use ChatGPT, Claude, or Gemini models in a blazing-fast terminal IDE.**

[![Download for macOS](https://img.shields.io/badge/Download-macOS-000000?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/mastershivek07/sg-code/releases/latest)
[![Download for Windows](https://img.shields.io/badge/Download-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/mastershivek07/sg-code/releases/latest)

---

</div>

## What is SG CODE?

SG CODE is a desktop application that gives you an AI coding assistant right in your terminal. Think of it as having a senior developer pair-programming with you — it can read your code, edit files, run commands, and reason about your entire project.

Built on the same architecture as Claude Code, but with multi-provider support and a native desktop experience.

**No API keys needed.** Sign in with your existing ChatGPT or Google account.

## Features

- **Multi-Provider Support** — Choose between ChatGPT (OpenAI) or Google AI (Claude, Gemini) models
- **Native Terminal** — Full xterm.js terminal with 256-color support, not a web wrapper
- **Multi-Tab Sessions** — Run multiple coding sessions side by side
- **Model Switching** — Switch between models on the fly (`/model`)
- **File Browser** — Built-in sidebar file explorer
- **Auto-Updates** — Always stay on the latest version via GitHub Releases
- **Cross-Platform** — macOS (Intel + Apple Silicon) and Windows (x64)
- **Privacy-First** — Your code stays on your machine; only explicit AI requests go to the provider

## Supported Models

### ChatGPT Provider (OpenAI)
| Model | Description |
|-------|-------------|
| `gpt-5.4` | GPT-5.4 — flagship, reasoning + vision |
| `gpt-5.4-pro` | GPT-5.4 Pro — extended reasoning (Pro plan) |
| `gpt-5.4-mini` | GPT-5.4 Mini — fast reasoning |
| `gpt-5.4-nano` | GPT-5.4 Nano — fastest |
| `gpt-5.2` | GPT-5.2 — previous gen reasoning |
| `gpt-5.2-pro` | GPT-5.2 Pro — previous gen extended |
| `gpt-4.1` | GPT-4.1 — legacy all-rounder |
| `gpt-4.1-mini` | GPT-4.1 Mini — legacy fast |
| `gpt-5.4-codex` | Codex GPT-5.4 via ChatGPT backend |
| `gpt-5.4-mini-codex` | Codex GPT-5.4 Mini |
| `gpt-5.3-codex` | Codex GPT-5.3 |
| `gpt-5.2-codex` | Codex GPT-5.2 |

### Google Provider (Antigravity)
| Model | Description |
|-------|-------------|
| `claude-opus-4-6-thinking` | Most capable reasoning model |
| `claude-sonnet-4-6-thinking` | Fast reasoning |
| `claude-sonnet-4-6` | Fast + capable (default) |
| `gemini-3.1-pro-high` | Gemini 3.1 Pro — high quality |
| `gemini-3.1-flash` | Gemini 3.1 Flash — fast |
| `gemini-3-flash` | Gemini 3 Flash |

## Quick Start

1. **Download** the latest release for your platform
2. **Install** — drag to Applications (macOS) or run the installer (Windows)
3. **Launch** SG CODE
4. **Choose your provider** — ChatGPT or Google (Antigravity)
5. **Sign in** with your account
6. **Start coding** — open a folder and ask the AI anything

## How It Works

SG CODE runs a local proxy that translates between your AI provider account and the coding agent. Everything runs on your machine — your code never leaves your computer (except what you explicitly send to the AI model).

```
┌─────────────┐     ┌──────────────┐     ┌─────────────────┐
│  SG CODE    │────▶│  Local Proxy  │────▶│  ChatGPT / GCP  │
│  Terminal   │◀────│  (localhost)  │◀────│  AI Models      │
└─────────────┘     └──────────────┘     └─────────────────┘
     Your machine         Your machine         Cloud API
```

## Project Structure

```
sg-code-v2/
├── main.js              # Electron main process
├── preload.js           # IPC bridge
├── proxy.mjs            # ChatGPT OAuth proxy (port 4141)
├── cli-bundle.mjs       # Bundled AI coding agent
├── supabase.js          # Usage tracking & entitlements
├── afterPack.js         # Cross-platform native binary cleanup
├── renderer/
│   ├── index.html       # Main window
│   ├── app.js           # Tab/session management, xterm.js
│   └── styles.css       # Green terminal theme
├── antigravity-proxy/   # Google OAuth proxy (port 4142)
│   └── src/
├── assets/              # App icons
└── package.json         # Electron + electron-builder config
```

## Building from Source

### Prerequisites
- Node.js 18+
- npm

### Install Dependencies
```bash
npm install
```

### Run in Development
```bash
npm start
```

### Build Installers
```bash
# macOS
npm run build

# Windows (from macOS or Windows)
npm run build:win

# All platforms
npm run build:all
```

Installers are output to the `dist/` folder.

## System Requirements

| | macOS | Windows |
|---|---|---|
| **OS Version** | macOS 12+ | Windows 10+ |
| **Architecture** | Intel / Apple Silicon | x64 |
| **Disk Space** | ~250 MB | ~250 MB |
| **Account** | ChatGPT or Google account | ChatGPT or Google account |

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + N` | New tab |
| `Cmd/Ctrl + W` | Close tab |
| `Cmd/Ctrl + B` | Toggle sidebar |
| `Cmd/Ctrl + 1-9` | Switch to tab |
| `/model` | Switch AI model |
| `/help` | Show all commands |

## FAQ

**Is this free?**
Yes, SG CODE is free. You use your own ChatGPT or Google account for AI access.

**Does it send my code to third parties?**
SG CODE runs entirely on your machine. The only external calls are to the AI model provider you chose (OpenAI or Google), and only when you actively ask the AI for help.

**Can I use it offline?**
The terminal works offline, but AI features require an internet connection to reach the model provider.

**Is this open source?**
Yes — the source code is available in this repository. The AI coding engine is based on open-source technology.

## License

MIT — see [LICENSE](LICENSE) for details.

---

<div align="center">

**Made with ⚡ by SG**

[Report Bug](https://github.com/mastershivek07/sg-code/issues) · [Request Feature](https://github.com/mastershivek07/sg-code/issues)

</div>
