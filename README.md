# Whisper-subtitle

Whisper-Subtitle is a Python-based tool that automates the process of extracting audio from video files, optionally denoising the audio, and generating subtitle files in SRT format using OpenAI's Whisper model. This repository leverages libraries such as PyTorch, Torchaudio, Transformers, and Denoiser to deliver high-quality transcription and subtitle generation.

## Features

- **Audio Extraction**: Extracts audio from video files using `ffmpeg`.
- **Noise Reduction**: Optionally reduces background noise in audio using a pretrained denoiser model.
- **Transcription**: Utilizes OpenAI's Whisper model for accurate speech-to-text transcription.
- **Subtitle Generation**: Creates `.srt` subtitle files with timestamped transcripts.

## Prerequisites

- Python 3.8 or higher
- [FFmpeg](https://ffmpeg.org/download.html) installed and added to your system's PATH.
- NVIDIA or AMD GPU with CUDA or ROCm support (optional, for faster processing)

## Notes

* A minimum of **16GB VRAM** is recommended to achieve high-quality subtitle materials.
* Whisper inherently has issues with generating precise timestamps. As a result, accurate timestamps may not always be produced, and a review is necessary.
* In certain languages, the **large-v2** model outperforms the **large-v3** model. This is influenced by the pseudo-labeled training method. For example, tests have confirmed that the large-v2 model delivers stronger performance for Japanese.
