# Single-cell RNA-seq Analysis of Immune Cells

This repository contains the code and visualizations from my analysis of scRNA-seq data, where I focused on identifying distinct immune cell types—especially different subsets of NKT and T cells.

## Why this project?

I wanted to explore how single-cell transcriptomics can reveal subtle differences in immune cell populations. Specifically, I was interested in characterizing NKT cells (both immature and mature), as well as comparing them with other closely related cell types like γδ T cells, CD8 T cells, NK cells, macrophages, etc.

## Main Steps

1. **Preprocessing**
   - Filtered out low-quality cells (too few genes or too much mitochondrial content).
   - Normalized the data and log-transformed it.

2. **Dimensionality Reduction**
   - Ran PCA and UMAP to visualize the data in 2D.

3. **Clustering**
   - Used the Leiden algorithm to find clusters of cells based on their gene expression profiles.

4. **Finding Marker Genes**
   - Identified genes uniquely expressed in each cluster to help understand what each one might represent biologically.

5. **Manual Annotation**
   - Based on known immune cell markers, I annotated the clusters as:
     - Cluster 0: Mature NKT cells
     - Cluster 1: Immature NKT cells
     - Cluster 2: NK cells
     - Cluster 3: γδ T cells
     - Cluster 4: CD8 T cells
     - Cluster 5: Macrophages
     - Cluster 6: Double Negative T cells
     - Cluster 7: Cycling T cells

6. **Visualization**
   - Used UMAP to visualize the annotated clusters.
   - Customized color palettes (e.g., `tab10`, `Set2`, `Paired`) to distinguish groups clearly.

## Tools

- Python (Scanpy, Pandas, Seaborn, Matplotlib)
- Google Colab (for easier sharing and GPU acceleration)

## Takeaways

The pipeline successfully separated biologically meaningful clusters. The marker gene expression matched expectations based on literature, giving confidence in the annotations. UMAPs were especially helpful in visualizing developmental trajectories and cluster separations.

## Files

- `notebook.ipynb`: The full analysis notebook.
- `figures/`: Contains UMAPs and marker expression plots.
- `README.md`: This file.

## Notes

This project could be extended by:
- Running pathway enrichment on markers.
- Comparing the cell types across different experimental conditions.
- Incorporating other data types (e.g., spatial data or TCR sequences).

## Author

Chinmayee Kalle  
Savitribai Phule Pune University  
MSc Biotechnology & Bioinformatics  
