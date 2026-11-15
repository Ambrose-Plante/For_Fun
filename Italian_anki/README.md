# Italian_anki

## Overview

This notebook automates creation of an Italian language-learning Anki deck from spreadsheet vocabulary. It reads paired English/Italian content, calls text-to-speech routines to create pronunciation audio, and defines genanki note/card templates for two-way review. Image-generation helper code is also present, making the notebook capable of enriching cards with generated media even though that is not the core data transformation. Generated assets are attached to the package and written into an Anki .apkg deck.

## Algorithmic workflow

1. Read vocabulary sheet
2. Synthesize audio/media
3. Instantiate Anki notes
4. Create reverse-direction cards
5. Attach assets
6. Package deck
