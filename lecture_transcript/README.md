# lecture_transcript

## Overview

This notebook automates transcription of medical school lecture-video files. FFmpeg is used to extract an audio stream from video into an audio format suitable for transcription, after which the OpenAI Whisper command-line tool is invoked. Whisper's official repository documents this direct audio-file transcription workflow. The notebook removes unwanted sidecar output formats and moves the plain-text transcript into a designated transcript directory.

## Algorithmic workflow

1. Enumerate videos
2. FFmpeg audio extraction
3. Invoke Whisper
4. Retain text output
5. Clean sidecars
6. Move transcript files
