# double_word_game

## Overview

This notebook solves a small dictionary word puzzle by searching for words containing exactly one adjacent duplicated letter of a candidate character. When such a double occurrence is found, one copy is removed, and the resulting character sequence is reversed. The algorithm then tests whether that reversed string is itself present in the loaded word list. Qualifying original/transformed word pairs are printed.

## Algorithmic workflow

1. Iterate dictionary
2. Detect adjacent duplicate
3. Collapse duplicate
4. Reverse string
5. Dictionary-membership test
6. Report pair
