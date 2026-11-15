# compare_gene_names

## Overview

This notebook performs a simple overlap operation between two gene-related CSV tables. It iterates over gene names from one dataset and compares them for exact equality against identifiers in a reference table. When a match is found, selected fields, including a later reference-table column, are copied into the output record. Matching rows are collected and finally written as overlapping_genes.csv.

## Algorithmic workflow

1. Read two CSVs
2. Iterate query genes
3. Exact identifier comparison
4. Select reference fields
5. Collect matches
6. Save CSV
