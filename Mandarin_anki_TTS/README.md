# Mandarin_anki_TTS

## Overview

This notebook performs the same general flashcard automation for Mandarin vocabulary, with Google Cloud text-to-speech producing Mandarin pronunciation audio. Spreadsheet rows supply the paired language content, and genanki models define cards that test both directions. The program creates media files, references those media files from card fields, and bundles them into a distributable Anki deck. Image-generation helper code is also included as an optional enrichment path.

## Algorithmic workflow

1. Load Mandarin/English pairs
2. TTS synthesis
3. Construct bidirectional cards
4. Attach MP3s
5. Write .apkg
6. Secure credentials separately
