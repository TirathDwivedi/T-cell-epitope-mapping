# T-cell-epitope-mapping
# Mapping scored peptides onto the viral proteome
To map scored BKV epitopes onto different BKV antigens
This Python script performs an analysis of epitopes within protein sequences and visualizes the scores of epitopes at each position in the protein sequence.

## Dependencies

- Pandas (imported as pd)
- Seaborn (imported as sns)
- Matplotlib.pyplot (imported as plt)
- NumPy (imported as np)

## Usage
1. Make sure you have the necessary data files:
BKV epitope lengths.xlsx: File containing epitope sequences.
BKV protein lengths.xlsx: File containing protein sequences.
2. Run the script by executing the provided code in a Python environment.
3. The script will read the epitope and protein sequences from the Excel files, merge them based on the protein name column, and calculate an epitope score at each position in the protein sequence.
4. It generates a visualization for each protein present in the dataset, displaying the score distribution of epitopes along the protein sequence.

## Code Description

A. Data Reading and Merging:
  1. Reads epitope sequences from 'BKV epitope lengths.xlsx' and protein sequences from 'BKV protein lengths.xlsx'.
  2. Merges the epitopes and proteins based on the protein name column.

B. Epitope Score Calculation:
  1. Calculates the score of each epitope at every position in the protein sequence.
  2. Scores are calculated based on matches between epitope sequences and the protein sequence.

C. Visualization:
  1. Generates a stacked area plot for each protein showing the distribution of epitope scores along its sequence.
  2. Colors in the plot represent the epitope score intensity.

D. Output
  The script generates visual plots for each protein's epitope score distribution. Each plot shows the protein name on the x-axis and the epitope score on the y-axis.

# Mapping RF values onto the viral proteome


# Sequence conservation and cross-reactivity analysis
