### README ###
# Tirath Raj Dwivedi
# 24/11/2023
#

# Project Description
To map average RF values obtained from the Immunome Browser (available on IEDB) onto different BKV antigens

This Python script visualizes the response frequency (RF) values of a protein sequence based on data obtained from an Excel file containing RF values for specific protein sequences.

## Dependencies

- Pandas (imported as pd)
- Matplotlib.pyplot (imported as plt)
- Matplotlib.ticker.MaxNLocator (imported as MaxNLocator)

Usage

1. Ensure you have the necessary data files:

BKV Large T_average RF values.xlsx: Excel file containing RF values for protein sequences.
BKV Large T.fa: File containing the full protein sequence.

2. Run the script by executing the provided code in a Python environment.

3. The script reads RF values from the Excel file and retrieves the full protein sequence from the provided file.

4. It creates a dictionary of RF values for each position in the protein sequence based on the provided data.

5. The script generates a plot displaying the response frequency along the positions in the protein sequence.

Code Description

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