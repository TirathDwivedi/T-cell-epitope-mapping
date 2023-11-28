### README ###
# Tirath Raj Dwivedi
# 24/11/2023
#

# Project Description

This project provides a set of Python scripts for analyzing JCV (John Cunningham Virus) genomic data and visualising epitope conservation. It performs various tasks such as extracting information from GenBank files, analyzing epitopes, calculating conservation percentages, and visualizing the conservation of epitopes.

Requirements:
Python 3.x
Pandas
BioPython (for GenBank file parsing)
Matplotlib
Seaborn

Files:
1. extract_genomic_data.py
Purpose: Extracts information from JCV GenBank files and stores relevant data into a Pandas DataFrame.
Usage: Execute this script to process GenBank files and generate an Excel file containing strain names, gene names, and protein sequences.

2. analyze_epitopes.py
Purpose: Analyzes epitopes and matches them with protein sequences from the extracted data.
Usage: Requires JCV_strains_protein_sequences.xlsx and JCV_scored_epitopes.xlsx. Matches epitopes with protein sequences and creates a new Excel file (results_JCV_scored_epitopes.xlsx) containing matched epitopes, gene names, and strains.

3. calculate_conservation.py
Purpose: Calculates conservation percentages of scored epitopes.
Usage: Reads % conservation_of_scored_epitopes.xlsx and computes conservation percentages for each epitope. Outputs a series of percentages.

4. visualize_conservation.py
Purpose: Visualizes the conservation of epitopes in a bar plot.
Usage: Reads results_JCV_scored_epitopes.xlsx to visualize epitope conservation percentages. Generates a bar plot (conservation.png) displaying conservation percentages categorized by epitopes.

Instructions:
Running the Scripts:

Ensure all required packages are installed (Pandas, BioPython, Matplotlib, Seaborn).
Run each script in the specified order for a complete analysis of JCV genomic data.
Input Files:

Ensure GenBank files (JCV GenBank.gb) are available for data extraction. 
JCV_scored_epitopes.xlsx and % conservation_of_scored_epitopes.xlsx are needed for epitope analysis and conservation calculation.
Output Files:

Running the scripts generates various output files:
JCV_strains_protein_sequences.xlsx: Extracted data from GenBank files.
results_JCV_scored_epitopes.xlsx: Matched epitopes with gene names and strains.
pivot_table_JCV_scored_epitopes.xlsx: Pivot table summarizing epitope occurrences in strains.
conservation.png: Visualization of epitope conservation percentages.

Adjustments:

Modify input file names or paths in the scripts if the file locations change.
Tweak parameters or formatting in the visualization script for different display preferences.