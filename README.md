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
To map average RF values obtained from the Immunome Browser (available on IEDB) onto different BKV antigens
This Python script visualizes the response frequency (RF) values of a protein sequence based on data obtained from an Excel file containing RF values for specific protein sequences.

## Dependencies

- Pandas (imported as pd)
- Matplotlib.pyplot (imported as plt)
- Matplotlib.ticker.MaxNLocator (imported as MaxNLocator)

## Usage

1. Ensure you have the necessary data files:
BKV Large T_average RF values.xlsx: Excel file containing RF values for protein sequences.
BKV Large T.fa: File containing the full protein sequence.

2. Run the script by executing the provided code in a Python environment.
3. The script reads RF values from the Excel file and retrieves the full protein sequence from the provided file.
4. It creates a dictionary of RF values for each position in the protein sequence based on the provided data.
5. The script generates a plot displaying the response frequency along the positions in the protein sequence.

## Code Description

A. Data Loading and Preparation:
  1. Reads RF values from 'BKV Large T_average RF values.xlsx'.
  2. Loads the full protein sequence from 'BKV Large T.fa'.

B. RF Value Mapping:
  1. Maps the RF values to their corresponding positions in the protein sequence.
  2. Creates a dictionary (rf_dict) containing the maximum RF value for each position.

C. Visualization:
  Generates a line plot showing the RF values along the protein sequence positions.

D. Plot Customization:
  1. Sets labels for x and y axes.
  2. Adjusts the tick parameters, axis limits, and plot aesthetics for better visualization.

E. Output
  The script generates a line plot where the x-axis represents the positions in the protein sequence, and the y-axis represents the response frequency values.

# Sequence conservation and cross-reactivity analysis
