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
## Sequence conservation
This project provides a set of Python scripts for analyzing BKV (BK Virus) genomic data and visualising epitope conservation. It performs various tasks such as extracting information from GenBank files, analyzing epitopes, calculating conservation percentages, and visualizing the conservation of epitopes.

## Dependencies:
Python 3.x
Pandas
BioPython (for GenBank file parsing)
Matplotlib
Seaborn

## Files:
1. extract_genomic_data.py
Purpose: Extracts information from BKV GenBank files and stores relevant data into a Pandas DataFrame.
Usage: Execute this script to process GenBank files and generate an Excel file containing strain names, gene names, and protein sequences.

2. analyze_epitopes.py
Purpose: Analyzes epitopes and matches them with protein sequences from the extracted data.
Usage: Requires BKV_strains_protein_sequences.xlsx and BKV_scored_epitopes.xlsx. Matches epitopes with protein sequences and creates a new Excel file (results_BKV_scored_epitopes.xlsx) containing matched epitopes, gene names, and strains.

3. calculate_conservation.py
Purpose: Calculates conservation percentages of scored epitopes.
Usage: Reads % conservation_of_scored_epitopes.xlsx and computes conservation percentages for each epitope. Outputs a series of percentages.

4. visualize_conservation.py
Purpose: Visualizes the conservation of epitopes in a bar plot.
Usage: Reads results_BKV_scored_epitopes.xlsx to visualize epitope conservation percentages. Generates a bar plot (conservation.png) displaying conservation percentages categorized by epitopes.

## Instructions:
Running the Scripts:
Ensure all required packages are installed (Pandas, BioPython, Matplotlib, Seaborn).
Run each script in the specified order for a complete analysis of BKV genomic data.

## Input Files:
Ensure GenBank files (BKV GenBank.gb) are available for data extraction.
BKV_scored_epitopes.xlsx and % conservation_of_scored_epitopes.xlsx are needed for epitope analysis and conservation calculation.

## Output Files:
Running the scripts generates various output files:
BKV_strains_protein_sequences.xlsx: Extracted data from GenBank files.
results_BKV_scored_epitopes.xlsx: Matched epitopes with gene names and strains.
pivot_table_BKV_scored_epitopes.xlsx: Pivot table summarizing epitope occurrences in strains.
conservation.png: Visualization of epitope conservation percentages.

## Adjustments:

Modify input file names or paths in the scripts if the file locations change.
Tweak parameters or formatting in the visualization script for different display preferences.

## Cross-reactivity
To identify cross-reactivity of BKV epitopes across different strains of JCV
This Python script aims to analyze cross-reactive epitopes between BKV and JCV by matching epitopes from one dataset with protein sequences from another dataset. The analysis involves reading Excel files containing epitopes and protein sequences, identifying matches, and generating pivot tables to summarize the occurrence of epitopes across different strains.

## Dependencies:
Python 3.x
Pandas
Seaborn
Regular Expressions (re)

## Files:

1. crossreactive_epitope_analysis.py
Purpose: Matches epitopes from one dataset with protein sequences from another dataset to identify cross-reactive epitopes between BKV and JCV.
Usage: Execute this script after placing the respective Excel files (BKV_scored_epitopes.xlsx and JCV_strains_protein_sequences.xlsx) in the same directory. It generates result files: results_BKV_crossreactive_epitopes.xlsx and pivot_table_BKV_crossreactive_epitopes.xlsx.

## Instructions:
Running the Script:
Ensure all required packages are installed (Pandas, Seaborn).
Place the input Excel files (BKV_scored_epitopes.xlsx and JCV_strains_protein_sequences.xlsx) in the same directory as the script.
Run the script to perform epitope matching and pivot table generation for cross-reactive epitopes.

## Input Files:
BKV_scored_epitopes.xlsx: Contains epitopes for BKV.
JCV_strains_protein_sequences.xlsx: Contains protein sequences for JCV strains.

## Output Files:
Upon execution, the script generates two output files:
results_BKV_crossreactive_epitopes.xlsx: Epitopes matched with gene names and strains.
pivot_table_BKV_crossreactive_epitopes.xlsx: Pivot table summarizing epitope occurrences across strains.

## Adjustments:
Modify the file paths in the script if the input file locations or names change.
Customize additional data processing or visualization as needed for further analysis.
