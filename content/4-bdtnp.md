---
title: BDTNP
nav: BDTNP
topics: Drosophila, Reconstruction, atlas
---

Here, we will use novoSpaRc to spatially reconstruct the early Drosophila embryo dataset, which is a whole organism tissue with stereotypical organization. Since a reference atlas of gene expression is provided, the reconstruction will performed with marker genes. 

## The Data

{% capture text %} You can download the data from the following link:
[BDTNP Dataset and the Jupyter Notebook](https://gigamove.rwth-aachen.de/en/download/f2c266d9bb9e7335e1ab471500320f6b)
{% endcapture %}
{% include card.html header="Data Download" text=text %}

{% capture text %}
You can use "dataset2_bdtnp.ipynb" as a starter.

The dataset consists of two files:
- dge.txt => this is the digital gene expression file
- geometry.txt => location coordinates
{% endcapture %}
{% include card.html header="Data Description" text=text %}

## Pseudocode script for basic reconstruction with marker genes

Import the required libraries

### Reading gene expression data
```
Read the single-cell gene expression matrix and the list of gene names from disk.
```

### Create a target space
#### Read the provided target space that was used in the paper
```
Read target space from disk
```

### Reconstruct the tissue
```
Construct Tissue object
Compute cost matrices
Compute OT of cells to locations for alpha=0.5
```

### Validate reconstruction against the reference atlas marker genes
```
Calculate Pearson correlations between the spatial predicted and original gene expression of marker genes
```

## Task 1: explore influence of number of marker genes
Perform reconstructions with 0, 1, 2 and 4 marker genes. How are the reconstructions affected? How does the de novo reconstruction look like?

## Task 2: explore influence of alpha parameter
Perform 5 reconstructions with different alpha parameter values: [0.25, 0.5, 0.75, 1] and one marker gene. How does alpha influence the reconstruction?

## Task 3: compute top spatially informative genes
Which are the top 10 spatially informative genes? What spatial expression patterns do they have?
