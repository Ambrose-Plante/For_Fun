# Cost_of_care_merged

## Overview

This notebook was used to extract and quantify cost-of-care survey responses from patients as part of a medical school collaboration with OBGYN providers trying to understand how language barriers affect pregnancy outcomes. It imports large dataset spreadsheets, performs structural checks on columns, and uses edit distance in parts of the header or label quality-control process. Response categories concerning cost discussions are counted and converted into percentages across comparison groups. The notebook produces publication-oriented bar charts that summarize those descriptive outcomes.

## Algorithmic workflow

1. Import sheets
2. Verify/clean fields
3. Classify responses
4. Count by study group
5. Compute proportions
6. Plot/export figures
