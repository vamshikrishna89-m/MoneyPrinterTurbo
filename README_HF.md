---
title: MoneyPrinterTurbo
emoji: 🤖
colorFrom: blue
colorTo: green
sdk: docker
app_port: 7860
pinned: false
license: mit
---

# MoneyPrinterTurbo - Hugging Face Spaces

Simply provide a topic or keyword for a video, and it will automatically generate the video copy, video materials, video subtitles, and video background music before synthesizing a high-definition short video.

## Configuration

Set these as **Secrets** in your Hugging Face Space settings:

| Secret Name | Description |
|------------|-------------|
| `OPENAI_API_KEY` | Your OpenAI API key (or other LLM provider key) |
| `OPENAI_BASE_URL` | Optional: custom OpenAI-compatible base URL |
| `LLM_PROVIDER` | LLM provider: openai, moonshot, deepseek, gemini, etc. |
| `PEXELS_API_KEYS` | Comma-separated Pexels API keys |
| `PIXABAY_API_KEYS` | Comma-separated Pixabay API keys |

## Usage

1. Open the Space
2. Enter a video topic/keyword
3. Configure video settings (language, duration, background music, etc.)
4. Click generate and wait for your video

## Tech Stack

- **Web UI**: Streamlit
- **Backend API**: FastAPI + Uvicorn
- **Video Processing**: MoviePy + FFmpeg + ImageMagick
- **TTS**: Azure TTS / Edge TTS / SiliconFlow TTS / Gemini TTS