# 🤖 My Jarvis AI Assistant Setup

This repository contains my customized implementation and configuration of
Jarvis, a locally running AI desktop assistant.

The objective of this project is to explore how local LLMs, speech AI,
vision models, cloud LLMs, and desktop automation can be orchestrated into
a practical AI assistant.

## Architecture

User Voice
    ↓
Wake Word Detection
    ↓
Speech-to-Text
Faster-Whisper (base.en)
    ↓
Intent / Request Processing
    ↓
AI Orchestration
    ├── Local LLM: Ollama
    │      └── Qwen 2.5 7B Instruct
    │
    ├── Advanced Planning
    │      └── Groq / Llama 3.3 70B
    │
    └── Vision
           └── LLaVA 7B
    ↓
Tools / Local Actions
    ↓
Response Generation
    ↓
Text-to-Speech
    ↓
Desktop UI

## 🧠 AI Stack

| Component | Technology | Purpose |
|---|---|---|
| Local LLM | Ollama + Qwen 2.5 7B Instruct | Local conversational AI and request processing |
| Advanced Planner | Groq / Llama 3.3 70B | Complex planning and reasoning |
| Vision | LLaVA 7B | Vision-language processing |
| Speech-to-Text | Faster-Whisper `base.en` | Converts voice input into text |
| Text-to-Speech | Local TTS | Voice responses |
| Desktop Application | Python / PySide6 | Jarvis desktop interface |
| Packaging | PyInstaller | Windows application packaging |

## 🔊 Speech-to-Text Enhancement

The default STT configuration was updated from:

`tiny.en`

to:

`base.en`

The goal is to improve English speech-recognition accuracy while retaining
local inference.

## 🏠 Local-First AI

The primary conversational model runs locally through Ollama using:

`qwen2.5:7b-instruct`

This allows the assistant to perform many AI interactions locally rather
than requiring every request to be sent to an external LLM service.

## 🧩 Hybrid AI Architecture

Jarvis uses a hybrid architecture.

Local models handle suitable everyday interactions, while specialized
models/services can be used for more demanding tasks.

This creates a practical balance between:

- Privacy
- Latency
- AI capability
- Cost
- Offline/local processing

## 👁️ Vision

LLaVA 7B is configured as the vision-language model for requests requiring
visual understanding.

## 🧠 Advanced Planning

For more complex planning workloads, the setup supports:

`Groq / Llama 3.3 70B`

This separates everyday local inference from more computationally demanding
reasoning tasks.

## 🔐 Security

Runtime configuration and credentials are intentionally kept outside the
Git repository.

The following should never be committed:

- API keys
- Access tokens
- `.env` files containing secrets
- Local application configuration containing credentials
- User-specific data

Only safe source code and documentation are maintained in the public
repository.

## 🎯 What I Learned

This project provided hands-on experience with:

- Local LLM deployment
- Ollama model management
- Voice AI
- Speech-to-text pipelines
- Vision-language models
- Hybrid local/cloud AI architecture
- AI model routing
- Desktop AI applications
- Python application packaging
- Git/GitHub version control

## 🚀 Next Steps

Potential future enhancements include:

- Agentic task execution
- Long-term memory
- RAG-based personal knowledge
- Calendar and email integration
- Browser automation
- Improved tool routing
- Multi-agent orchestration
- Additional privacy and security controls

---

This repository is based on the original Jarvis open-source project and
contains my own configuration, experimentation, and enhancements.