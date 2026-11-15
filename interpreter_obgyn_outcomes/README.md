# interpreter_obgyn_outcomes

## Overview

This notebook was written as part of a collaboration with OBGYN providers in order to analyze obstetric cohort data from multiple clinical sources related to interpreter use and delivery outcomes. CSV tables are loaded and categorical fields such as delivery type, diabetes, race, hypertension, insurance, and BMI-related values are converted into standardized representations through mapping functions. Records are joined using identifying fields and delivery timing, with exception paths identifying data that cannot be matched or categorized cleanly. The resulting records are assembled into a pandas data frame suitable for subsequent outcome comparisons. The main algorithm is deterministic clinical ETL and record linkage.

## Algorithmic workflow

1. Import clinical sources
2. Normalize categories
3. Parse numeric fields
4. Match patient/delivery records
5. Flag unmatched values
6. Assemble analysis cohort
