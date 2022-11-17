# Notebooks for running htFuncLib

## General overview:
### htFuncLib is split to two notebooks:
1. 01_htFuncLib_prepare_jobs.ipynb
2. 02_htFuncLib_aggregation_and_analysis.ipynb

## Step 0
### Before running notebook 01, you need to retrieve several files from a FuncLib run [FuncLib](https://funclib.weizmann.ac.il/bin/steps), which you can do at the webserver.
The files you need are:
- a refined PDB structure
- a PSSM
- resfiles (residue files) that describe a series of sequence spaces
- Rosetta flags file
- Ligand param files (optional)

## Step 1
Notebook 01 is here to create the data required to train the EpiNNet model in notebook 02.
The notebook consists of the following stages:
  1. imports and initial setup
  2. setting up initial parameters
  3. create the bubbles
  4. choose ∆∆G
  5. prepare and run design jobs
  6. run all jobs and aggregate scores

## Step 2
In notebook 02 you will train the EpiNNet model on the aggregated data, and then choose the sequence space you wish to test experimentally.
The notebook consists of the following stages:
  1. Imports and initial setup
  2. Setting up the initial paramteres
  3. Parse the score dataframe created by the 01 notebook
  4. Training the neural net model
  5. Rank mutaitons by EpiNNet
  6. Choose mutations
  7. Find the best sequence space
  8. Test 10k designs

## Required packages
- BioPython (1.78)
- lightgbm (3.2.1)
- matplotlib (3.1.1)
- numpy (1.20.2)
- pandas (1.2.3)
- seaborn (0.11.1)
- sklearn (0.0)
- tqdm (4.59.0)

## Please cite
1. Weinstein, J. Y.; Aldaravi, C. M. G.; Lipsh-Sokolik, R.; Hoch, S. Y.; Liebermann, D.; Nevo, R.; Weissman, H.; Petrovich-Kopitman, E.; Margulies, D.; Ivankov, D.; McCandlish, D.; Fleishman, S. J. Designed Active-Site Library Reveals Thousands of Functional GFP Variants. bioRxiv October 11, 2022, p 2022.10.11.511732. https://doi.org/10.1101/2022.10.11.511732.
2. Lipsh-Sokolik, R.; Khersonsky, O.; Schröder, S. P.; Boer, C. de; Hoch, S.-Y.; Davies, G. J.; Overkleeft, H. S.; Fleishmam, S. J. Modularly Designed Protein Fragments Combine into Thousands of Active and Structurally Diverse Enzymes. bioRxiv September 18, 2022, p 2022.09.17.508230. https://doi.org/10.1101/2022.09.17.508230.

