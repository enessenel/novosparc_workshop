---
title: Kidney Dataset
nav: Kidney
topics: Kidney, Reconstruction, de-novo
---

## Kidney Dataset

Here, we will use novoSpaRc to spatially reconstruct a single-cell dataset from whole kidney [1], which is a complex tissue with stereotypical organization. Since there is no reference atlas of gene expression, the reconstruction will performed de novo. 

{% capture text %} [1] Park, J. et al. Single-cell transcriptomics of the mouse kidney reveals potential cellular targets of kidney disease. Science 360, 758–763 (2018). {% endcapture %}
{% include card.html header="Overview" text=text %}

## Download the data
{% capture text %} You can download the data from the following link:
[Download Kidney Dataset](https://gigamove.rwth-aachen.de/en/download/60d8b33b09c0cc4da07783830380771d)

The dataset consists of three files:
- dge_normalized.txt => this is the digital gene expression file
- gene_names.txt => names of the genes
- hvg_839.txt => names of the highly variable genes that can be used in the processing
{% endcapture %}
{% include card.html header="Overview" text=text %}


## Pseudocode script for basic de novo reconstruction

Import the required libraries

```
# imports
%matplotlib inline
import novosparc

import os
import numpy as np
import pandas as pd
import random
import scanpy as sc
import matplotlib.pyplot as plt
import altair as alt
from scipy.spatial.distance import cdist, squareform, pdist
```

### Reading gene expression data
```
Read the single-cell gene expression matrix and the list of gene names from disk.
```

### Preprocess the data and subset cell number
```
Normalize the data by using scanpy
```

To get quickly setup our script, we subset our dataset to 3,000 cells. Make sure you use the following seed for reproducible results

```
random.seed(2022)
Subset dataset to 3000 cells
```

### Create a target space
#### First use the provided target space that was used in the paper
```
Read target space from disk
Subset target space to 2,000 locations
```

#### Alternatively (for task 3): create a new target space
```
Use the provided script to generate a target space of any country
```

### Reconstruct the tissue
```
Construct Tissue object
Compute cost matrices
Compute OT of cells to locations for alpha=0
```

### Validate reconstruction for different kidney compartments

## Task 1: explore influence of number of locations
For the same set of 5,000 cells (use same random seed) run 5 reconstructions with different number of locations. How robust are the resulting reconstruction?.

## Task 2: explore influence of number of cells
For a fixed target space perform 5 reconstructions with different number of cells. How is running time affected? How robust are the resulting reconstructions?

## Task 3: explore different target spaces
Setup different target spaces and explore the reconstructions. How are these affected from the shape of the target space? How robust are the reconstructions?

