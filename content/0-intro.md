---
title: Intro
nav: Intro
topics: novoSpaRc; Theory
---

## About novoSpaRc
Single-cell RNA-sequencing (scRNA-seq) technologies have revolutionized modern biomedical sciences. A fundamental challenge is to incorporate spatial information to study tissue organization and spatial gene expression patterns. 
novoSpaRc, a computational framework that probabilistically assigns cells to tissue locations by using the structural correspondence hypothesis, that cells in physical proximity share similar gene expression profiles. Given scRNA-seq data, novoSpaRc spatially reconstructs tissues based on this hypothesis, and optionally, by including a reference atlas of marker genes to improve reconstruction. 

{% include figure.html img="novosparcflow.png" alt="novoSpaRc Flowchart" caption="novoSpaRc Flowchart" width="100%" %}

## General Usage of novoSpaRc

To spatially reconstruct gene expression, novoSpaRc performs the following steps:

1. Read the gene expression matrix.
        Optional: select a random set of cells for the reconstruction.
        Optional: select a small set of genes (e.g. highly variable).

2. Construct the target space.

3. Setup the optimal transport reconstruction.
        Optional: use existing information of marker genes, if available.

4. Perform the spatial reconstruction.
        Assign cells a probability distribution over the target space.
        Derive a virtual in situ hybridization (vISH) for all genes over the target space.
5. Write outputs to file for further use, such as the spatial gene expression matrix and the target space coordinates.
    Optional: plot spatial gene expression patterns.
    Optional: identify and plot spatial archetypes.

## Important Links

{% include button.html text="Github Repo" link="https://github.com/rajewsky-lab/novosparc" color="info" %}

{% include button.html text="Documentation" link="https://novosparc.readthedocs.io/" color="info" %}

{% include button.html text="Tutorial" link="https://github.com/rajewsky-lab/novosparc/blob/master/reconstruct_drosophila_embryo_tutorial.ipynb" color="info" %}

## Publications

Gene Expression Cartography
M Nitzan*, N Karaiskos*, N Friedman†, N Rajewsky†
[Nature](https://www.nature.com/articles/s41586-019-1773-3) (2019)

novoSpaRc: flexible spatial reconstruction of single-cell gene expression with optimal transport
N Moriel*, E Senel*, N Friedman, N Rajewsky, N Karaiskos†, M Nitzan†
[Nature Protocols](https://www.nature.com/articles/s41596-021-00573-7) (2021)









