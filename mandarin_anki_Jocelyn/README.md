# mandarin_anki_Jocelyn

## Overview

This notebook creates Mandarin Anki cards using an existing human-recorded audio track from a native mandarin speaker. The mandarin speaker reads a long list of phrases while listening to a metronome. Every 4 beats a tone is played letting the speaker know to say the next phrase. Because the tempo of the metronome is known, the single wav file can be automatically cut at specified start/end boundaries are used to cut it into phrase-sized clips. Those clips are aligned by order with Mandarin/English entries obtained from the spreadsheet list. The program creates bidirectional Anki cards and attaches the corresponding recorded segment as media.

## Algorithmic workflow

1. Load source recording
2. Obtain phrase table
3. Slice by timestamps
4. Align clip with phrase
5. Construct cards
6. Package audio/deck
