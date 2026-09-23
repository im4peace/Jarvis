# 🤖 My Jarvis AI Assistant

My configuration and experiments with a fork of the [original Jarvis project](https://github.com/ndunl075/Jarvis). The original project provides the core voice assistant and desktop features.

My objective with this project is to experiment hands-on with local LLMs,
Voice AI, Vision AI, model routing, and desktop AI automation.

## What I changed

I changed the default Faster-Whisper speech-to-text model in the fork from `tiny.en` to `base.en`. The Ollama, vision, and optional Groq models listed below describe my configuration and experiments; they are not separate code features I developed.

The `qwen2.5:7b-instruct` model requires enough free memory to load. Listing a model does not mean I successfully ran every combination on my PC.

## Architecture

The following flow is a conceptual overview. The cloud planner is optional and requires an internet connection and provider credentials.

User Voice
    ↓
Wake Word Detection
    ↓
Speech-to-Text
    ↓
Faster-Whisper (base.en)
    ↓
AI Orchestration
    ├── Local LLM → Ollama / Qwen 2.5 7B Instruct
    ├── Advanced Planner → Groq / Llama 3.3 70B
    └── Vision → LLaVA 7B
    ↓
Tools / Local Actions
    ↓
Response
    ↓
Text-to-Speech
    ↓
Desktop UI

## AI Stack

| Component | Technology | Role |
|---|---|---|
| Local LLM | Ollama + Qwen 2.5 7B | Local conversational AI |
| Planner | Groq / Llama 3.3 70B | Advanced planning |
| Vision | LLaVA 7B | Visual understanding |
| Speech-to-Text | Faster-Whisper base.en | Voice transcription |
| Desktop UI | Python / PySide6 | Desktop interface |
| Packaging | PyInstaller | Windows executable |

## My Customizations

### Speech Recognition

Updated the default Faster-Whisper model from:

`tiny.en`

to:

`base.en`

as an experiment with a larger English speech-recognition model. It can use more resources than `tiny.en`.

### Local LLM

Configured Jarvis to use:

`qwen2.5:7b-instruct`

through Ollama for local inference.

### Vision

Configured:

`llava:7b`

for vision-language capabilities.

### Advanced Planning

Configured an optional Groq-hosted Llama model for planning experiments. When enabled, this component sends requests to a cloud provider and requires a working internet connection.

## Architecture Principles

The setup explores a hybrid AI architecture where different models can be
used according to the workload.

Key considerations include:

- Local-first processing
- Privacy
- Latency
- Cost
- Model specialization
- Offline capability
- Cloud escalation for complex workloads

## What I Learned

Through this project I gained hands-on experience with:

- Local LLM deployment using Ollama
- LLM model configuration and routing
- Voice AI and speech-to-text
- Vision-language models
- Hybrid local/cloud AI architecture
- Python desktop AI applications
- PyInstaller application packaging
- Git and GitHub version control

## Next Steps

Planned areas of experimentation:

- Agentic task execution
- Long-term memory
- RAG-based personal knowledge
- Browser automation
- Email and calendar integration
- Improved model routing
- Multi-agent orchestration

## Credits

This fork is based on the [original open-source Jarvis project by ndunl075](https://github.com/ndunl075/Jarvis). The original project provides the core application. My code change and setup experiments are described above.
