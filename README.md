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

**No API keys needed.** Sign in with your existing ChatGPT or Google account.

## Features

- **Multi-Provider Support** — Choose between ChatGPT (OpenAI) or Google AI (Claude, Gemini) models
- **Native Terminal** — Full xterm.js terminal with 256-color support, not a web wrapper
- **Multi-Tab Sessions** — Run multiple coding sessions side by side
- **Model Switching** — Switch between models on the fly (`/model`)
- **Auto-Updates** — Always stay on the latest version
- **Cross-Platform** — macOS and Windows

## Supported Models

### ChatGPT Provider
| Model | Description |
|-------|-------------|
| `gpt-5.3-codex` | Latest GPT coding model |

### Google Provider (Antigravity)
| Model | Description |
|-------|-------------|
| `claude-opus-4-6-thinking` | Most capable reasoning model |
| `claude-sonnet-4-6` | Fast + capable (default) |
| `gemini-2.5-pro` | Google's flagship model |
| `gemini-2.5-flash` | Fast and efficient |
| `gemini-3-pro-high` | Next-gen high quality |
| `gemini-3-flash` | Next-gen fast |
| + more | 14 models total |

## Quick Start

1. **Download** the latest release for your platform
2. **Install** — drag to Applications (macOS) or run the installer (Windows)
3. **Launch** SG CODE
4. **Sign in** with ChatGPT or Google
5. **Start coding** — open a folder and ask the AI anything

## How It Works

SG CODE runs a local proxy that translates between your AI provider account and the coding agent. Everything runs on your machine — your code never leaves your computer (except what you explicitly send to the AI model).

```
┌─────────────┐     ┌──────────────┐     ┌─────────────────┐
│  SG CODE    │────▶│  Local Proxy  │────▶│  ChatGPT / GCP  │
│  Terminal   │◀────│  (localhost)  │◀────│  AI Models      │
└─────────────┘     └──────────────┘     └─────────────────┘
     Your machine         Your machine         Cloud API
```

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
| `Cmd/Ctrl + T` | New tab |
| `Cmd/Ctrl + W` | Close tab |
| `/model` | Switch AI model |
| `/help` | Show all commands |
| `Cmd/Ctrl + ,` | Settings |

## FAQ

**Is this free?**
Yes, SG CODE is free. You use your own ChatGPT or Google account for AI access.

**Does it send my code to third parties?**
SG CODE runs entirely on your machine. The only external calls are to the AI model provider you chose (OpenAI or Google), and only when you actively ask the AI for help.

**Can I use it offline?**
The terminal works offline, but AI features require an internet connection to reach the model provider.

**Is this open source?**
The desktop app is distributed as a compiled application. The AI coding engine is based on open-source technology.

## License

SG CODE is free to use. See [LICENSE](LICENSE) for details.

---

<div align="center">

**Made with ⚡ by SG**

[Report Bug](https://github.com/mastershivek07/sg-code/issues) · [Request Feature](https://github.com/mastershivek07/sg-code/issues)

</div>
