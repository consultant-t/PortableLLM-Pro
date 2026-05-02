# PortableLLM-Pro ⚡

**PortableLLM-Pro** is a fully air-gapped, zero-dependency, plug-and-play Local AI 
environment designed to run seamlessly from your **local hard drive** or a 
**portable USB/SSD**. It bypasses complex installations by natively executing large 
language models directly on your hardware — no internet, no cloud, no compromise.

With a unified architecture, initialize your AI models once and choose to keep them 
on your system or carry them across Windows, macOS, and Linux PCs.

> *"Your AI. Your hardware. No cloud. No compromise."*

---

## 🚀 Core Features

- **Zero Dependency Setup:** Ships with portable Python and isolated engine binaries. 
  No system permissions, registry edits, or package managers required.
- **Cross-Platform Interoperability:** Uses an intelligent `Shared` volume system — 
  download your 5GB+ AI models *once*, and use them natively on Windows, macOS, and 
  Linux without duplication.
- **Unrestricted Inference:** Integrates fine-tuned open-source models for completely 
  unfiltered, unbiased interactions.
- **Network Proxied UI:** A custom Python HTTP server serves a blazing-fast dark mode 
  UI accessible from your phone or tablet on the same WiFi — no CORS configuration needed.
- **Hardware Accelerated:** Custom-compiled engine natively leverages AVX CPU 
  instructions, NVIDIA CUDA, or Apple Metal GPU accelerators dynamically across host machines.

---

## 💻 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **Storage** | 8 GB free (USB 3.0+) | 16 GB+ SSD |
| **RAM (2B/4B models)** | 8 GB | 16 GB |
| **RAM (9B/12B models)** | 16 GB | 32 GB |

---

## 📂 Folder Architecture

```text
PortableLLM-Pro/
 ├── 📁 Android    # Native Android (Termux) installers & launchers
 ├── 📁 Linux      # Native Ubuntu/Debian offline installers & launchers
 ├── 📁 Mac        # Native macOS offline installers & launchers
 ├── 📁 Windows    # Native Windows offline automatic UI menus
 └── 📁 Shared     # Unified Data System
      ├── 📁 bin         (Isolated executables per OS)
      ├── 📁 chat_data   (Cross-platform persistent conversation history)
      ├── 📁 models      (GGUF model weights & local database mapping)
      └── 📁 python      (Isolated portable Python environment)
```

---

## 🧠 Supported AI Models

PortableLLM-Pro includes a curated installer for the highest-quality locally 
operable open-source models:

| Model | Size | Best For |
|-------|------|----------|
| Gemma 2 2B Abliterated | ~1.6 GB | All devices, fast inference |
| Gemma 4 E4B Uncensored | ~5.34 GB | Deep reasoning, unrestricted |
| Qwen 3.5 9B Uncensored | ~5.2 GB | Complex tasks, raw answers |
| **Custom GGUF** | Any | Import any HuggingFace model |

---

## ⚙️ Quick Start

### Step 1 — Initialize the Engine

Navigate to your OS folder and run the install script:

| OS | Command |
|----|---------|
| **Windows** | Double-click `Windows/install.bat` |
| **macOS** | Drag `Mac/install.command` into Terminal → Enter |
| **Linux** | `bash Linux/install.sh` |
| **Android** | `bash Android/install.sh` (in Termux) |

> Downloads a ~50MB OS-specific execution engine into `Shared/bin`

### Step 2 — Download AI Models

Run via **Windows** (`install.bat`) for the interactive model catalog.  
Or manually place `.gguf` files from HuggingFace into `Shared/models`.

### Step 3 — Launch

| OS | Command |
|----|---------|
| **Windows** | `Windows/start-fast-chat.bat` |
| **macOS** | `Mac/start.command` |
| **Linux** | `bash Linux/start.sh` |
| **Android** | `bash Android/start.sh` |

Your browser opens automatically with the local Chat UI.

---

## 🏠 Local Disk Installation

Works perfectly as a lightweight local AI setup on your primary machine:

1. Download/clone this repo to any folder on your drive
2. Navigate to your OS folder
3. Run `install.bat` (or equivalent) and select your models
4. Run `start-fast-chat.bat` to begin

> Running from an internal SSD delivers near-instant model loading vs USB.

---

## 📱 Android Support (Termux)

Run the AI engine directly on your Android phone — no PC required!

**Requirements:**
- Termux from [F-Droid](https://f-droid.org/en/packages/com.termux/) (not Play Store)
- 6 GB+ RAM (8 GB+ recommended)
- ARM64 processor

**Setup:**
```bash
bash Android/install.sh
bash Android/start.sh
```

**Tips:**
- Run `termux-wake-lock` before starting
- Use the 2B model on devices under 12 GB RAM
- Keep Termux in the foreground
- Plug in your charger — LLM inference is battery intensive
- Expect ~3–10 tokens/sec on the 2B model

---

## 📶 LAN Mobile Access

Access the AI from your phone while your PC runs the engine:

1. Ensure PC and phone are on the same WiFi network
2. The terminal displays a **Network Access IP** (e.g., `http://192.168.1.15:3333`)
3. Open that URL in your mobile browser

> If pages don't load, allow port `3333` through Windows Firewall.

---

## 🛠️ Troubleshooting

| Issue | Fix |
|-------|-----|
| Script closes instantly on Windows | Disable App Execution Aliases or run via CMD / "Run as Administrator" |
| "Engine Not Found" error | Run the `install` script before `start` — it downloads the OS engine first |
| Slow generation speeds | Switch to the 2B model — ideal for older or RAM-limited machines |

---

## 📄 License

MIT License — © 2026 [consultant-t](https://github.com/consultant-t)

---

> *PortableLLM-Pro is built for computational freedom and privacy-first AI access. 
> Use responsibly.*