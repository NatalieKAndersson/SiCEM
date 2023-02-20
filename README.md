# SCEM <img src="https://github.com/NatalieKAndersson/SCEM/blob/main/Figures/SCEM.JPG" align = "right" width="180"/>
Single cell event matrix (SCEM) is an algorithm for event matrix generation from single cell whole genome copy number sequencing data. The event matrix can then be used to generate phylogenetic trees of the evolutionary relationship between individual cells.

<a href="https://zenodo.org/badge/latestdoi/297145258"><img src="https://zenodo.org/badge/297145258.svg" alt="DOI"></a>

When using the algorithm, please cite: 
bioRxiv 2022.04.01.486670

doi: https://doi.org/10.1101/2022.04.01.486670

## Setting up SCEM

SCEM can be installed by running the following lines of code

```
library(devtools)
devtools::install_github('NatalieKAndersson/SCEM')
library("SCEM")
```


## Example data set
The file "Example.xlsx" contains an example of what the data set might look like. Through single cell whole genome sequencing, the copy number of each 1 Mbp (mega base pair) segment of each chromosome in each individual cell is approximated. This results in a matrix with thousands of rows indicating the copy number for each chromosome segment in each analyzed cell. In S. Figure 1 an example of a small proportion of what such a matrix might look like is visualized.

- First column: The bin number.
- Second and third column: The start and end position for that bin.
- Fourth column: The chromosome.
- Fifth column and beyond: The cells. Each column corresponds to a single cell or group of cells, indicated by row two. For example C1_1 contains 20 cells with identical genomic profiles and C1_7 is a single cell having a unique genomic profile.
- Each matrix element is the copy number in that particular chromosomal segment.

<img src="https://github.com/NatalieKAndersson/SCEM/blob/main/Figures/Exampledata.JPG" width="700"/>

