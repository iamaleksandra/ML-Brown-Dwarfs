# Brown Dwarf Machine Learning Dataset

Dataset for machine learning identification of L and T brown dwarfs in large photometric sky surveys.

This repository provides the dataset used in the peer-reviewed publication:

Avdeeva, A. (2024)  
Machine learning methods for the search for L&T brown dwarfs in the data of modern sky surveys  
Astronomy and Computing, Volume 46, 100744  
DOI: https://doi.org/10.1016/j.ascom.2023.100744  
arXiv: https://arxiv.org/abs/2308.03045

---

## Scientific context

Brown dwarfs are substellar objects located between stars and planets in mass. Identifying them efficiently in modern photometric surveys requires robust machine learning methods applied to multi-band photometric data.

This dataset was compiled to train and evaluate machine learning classifiers for brown dwarf identification.

It combines photometry from:

• Pan-STARRS DR1  
• 2MASS  
• WISE  

and includes both brown dwarfs and non-brown dwarf objects.

---

## Dataset description

File:

dataset_bd_wnames.csv

Contains:

• photometric magnitudes  
• magnitude uncertainties  
• object identifiers  
• class labels  

The dataset corresponds to the pre-processed data before:

• data augmentation  
• missing value imputation  

This ensures full reproducibility of the preprocessing and machine learning pipeline described in the paper.

---

## Dataset statistics

Total objects: 5669

Classes:

• Positive class: L and T brown dwarfs  
• Negative class: other stellar types  

Features include magnitudes in multiple photometric bands and derived colour indices.

---

## Usage

Example loading in Python:

```python
import pandas as pd

df = pd.read_csv("dataset_bd_wnames.csv")
print(df.head())
