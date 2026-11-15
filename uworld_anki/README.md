# uworld_anki

## Overview

This notebook converts specially formatted study text into an Anki question deck. clinical questions are fed into chatgpt to create prompts. A parser recognizes formatting markers—particularly bold-style lines—and separates the input into question/answer records. Those records are inserted into a simple genanki note model with front/back card templates. The assembled notes are added to a deck and written to an .apkg archive.

## Algorithmic workflow

1. Read formatted text
2. Detect question/answer boundaries
3. Build record pairs
4. Instantiate Anki notes
5. Add to deck
6. Export package
