# BnB_transcript

## Overview

This notebook was created to match Boards and Beyond video transcripts according to how well they correspond to medical school lecture materials so that the appropriate thrid party resources can be watched in adjunct to the lectures. It reads lecture PDFs and transcript text, normalizes words, and uses edit distance so that a transcript word can match a query even when transcription or spelling is slightly imperfect. For each lecture-derived term, transcript sentences or words are scanned and counted when their Levenshtein distance falls within a chosen tolerance. Those approximate matches are aggregated into per-video scores, allowing the notebook to rank the strongest candidate videos for each lecture. The resulting match lists and cross-lecture frequency summaries are written into Google Sheets for review.

## Algorithmic workflow

1. Extract PDF vocabulary
2. Clean transcript text
3. Fuzzy word comparison
4. Aggregate match scores
5. Rank videos
6. Publish worksheets
