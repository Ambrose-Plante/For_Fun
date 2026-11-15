# For_Fun — Utilities and Independent Research Projects

A collection of smaller coding projects, research prototypes, automation scripts, and educational experiments. The projects span language learning, clinical and scientific data analysis, media processing, Google Drive utilities, and algorithmic puzzles. Each folder contains its own source code and a project-specific README.

These are independent experiments rather than components of the [Maximus music-generation pipeline](https://github.com/Ambrose-Plante/Music-generative-AI).

## Project directory

| Category | Project | Description |
| --- | --- | --- |
| Language learning | [`Italian_anki`](Italian_anki/) | Generates Italian vocabulary Anki decks from spreadsheet data, with pronunciation audio and optional media. |
| Language learning | [`Mandarin_anki_TTS`](Mandarin_anki_TTS/) | Builds Mandarin/English Anki cards and synthesizes pronunciation audio using Google Cloud text-to-speech. |
| Language learning | [`mandarin_anki_Jocelyn`](mandarin_anki_Jocelyn/) | Segments a human-recorded Mandarin audio track using known recording timing and attaches clips to bilingual Anki cards. |
| Study tools | [`uworld_anki`](uworld_anki/) | Parses specially formatted question-and-answer study material into an Anki deck. |
| Transcription | [`BnB_transcript`](BnB_transcript/) | Matches medical lecture materials to Boards & Beyond video transcripts using approximate text matching and ranks relevant videos. |
| Transcription | [`lecture_transcript`](lecture_transcript/) | Extracts lecture-video audio and automates speech transcription with Whisper. |
| Media processing | [`video_to_mp3`](video_to_mp3/) | Sorts and processes video files, converts or extracts audio, and prepares recordings for transcription. |
| Data utilities | [`search_google_drive`](search_google_drive/) | Searches files in a mounted Google Drive hierarchy using filesystem and text-search commands. |
| Data utilities | [`export_google_drive`](export_google_drive/) | Recursively collects selected source-code file types from Google Drive into a ZIP archive while retaining relative paths. |
| Data utilities | [`compare_gene_names`](compare_gene_names/) | Performs exact gene-name matching between two CSV datasets and exports overlapping records. |
| Algorithmic puzzles | [`double_word_game`](double_word_game/) | Finds English word pairs by removing one letter from an adjacent double and reversing the remaining characters. |
| Clinical analysis | [`interpreter_obgyn_outcomes`](interpreter_obgyn_outcomes/) | Harmonizes and joins clinical obstetric records for analysis of interpreter use and delivery outcomes. |
| Physiological signals | [`polysomnography_parsing`](polysomnography_parsing/) | Explores EDF polysomnography recordings, signal metadata, sample timing, and waveform visualization. |
| Machine-learning reference | [`The_Annotated__Attention_is_All_You_Need`](The_Annotated__Attention_is_All_You_Need/) | Educational/reference implementation and walkthrough of the encoder–decoder Transformer architecture. |

## Featured experiment: double_word_game

[`double_word_game/double_word_game.py`](double_word_game/double_word_game.py) explores an unusual dictionary transformation:

1. Take a word containing a character that occurs **exactly twice**, in adjacent positions.
2. Remove one of those adjacent copies.
3. Reverse the remaining letters.
4. Check whether the reversed result is also a dictionary word.

For example, `balls` becomes `bals` after removing one `l`, then becomes `slab` when reversed. Other matches include:

| Input word | Result |
| --- | --- |
| `balls` | `slab` |
| `boons` | `snob` |
| `dwell` | `lewd` |
| `gulls` | `slug` |
| `pills` | `slip` |
| `spill` | `lips` |

### Dictionary test

A local test using an **alphabetic, 4–7-letter subset of the CMU Pronouncing Dictionary** produced **412 input/result matches**. The result CSV was provided separately and is not currently committed to this repository. Dictionary contents matter: pronunciation dictionaries can include proper names, uncommon terms, and spelling variants, so not every match will be a common English word.

The current script requires a `words.txt` file with one word per line, in the working directory, and the NumPy package:

```bash
cd double_word_game
python -m pip install numpy
python double_word_game.py
```

The script prints `original / transformed` when both words are in the supplied list. Its final `'accreditation' in word_list` expression is an interactive membership check and is not printed when the script runs normally. The algorithm returns after the **first** qualifying repeated letter (chosen in the order returned by `np.unique`). Dictionary membership currently scans a Python list, so converting the list to a `set` would speed up tests on larger word lists.

## Notes

- The folders contain **research and prototype code**, not necessarily complete or maintained production applications. Some scripts depend on local datasets, Colab/Google Drive paths, external tools, credentials, or older Python libraries.
- Before reusing the Anki/TTS projects, inspect any API integrations for historical embedded credentials and use environment variables or a secrets manager instead.
- The annotated Transformer project is reference/educational material; check the relevant upstream license and attribution before redistribution.

See each linked project README for a more detailed explanation of its algorithm and processing steps.
