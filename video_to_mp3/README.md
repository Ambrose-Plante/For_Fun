# video_to_mp3

## Overview

This notebook prepares video or recorded-media files for audio processing and transcription. Filename utilities extract numeric/textual components so files can be processed in a predictable natural order instead of arbitrary filesystem order. Audio is extracted or converted into MP3-compatible form using media tooling such as pydub/FFmpeg, with transcription-related setup appearing in the workflow. Whisper-related commands provide a path from those normalized audio files to text; Whisper officially supports direct transcription of common audio files. 10 The notebook is therefore a media-ingestion utility whose main algorithms are ordering, conversion, and preparation for speech recognition.

## Algorithmic workflow

1. Enumerate/sort media
2. Extract audio
3. Normalize/convert format
4. Prepare temporary MP3
5. Optionally invoke transcription
6. Organize outputs
