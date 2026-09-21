# 🤖 My Jarvis AI Assistant

A customized local/hybrid AI desktop assistant built on the open-source
Jarvis project.

My objective with this project is to experiment hands-on with local LLMs,
Voice AI, Vision AI, model routing, and desktop AI automation.

## Architecture

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

to improve English speech-recognition accuracy.

### Local LLM

Configured Jarvis to use:

`qwen2.5:7b-instruct`

through Ollama for local inference.

### Vision

Configured:

`llava:7b`

for vision-language capabilities.

### Advanced Planning

Configured a Groq-hosted Llama model for more demanding planning tasks,
creating a hybrid local/cloud AI architecture.

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

This project is based on the original open-source Jarvis project.

This fork documents my own configuration, experimentation, and enhancements
while preserving attribution to the original project.
