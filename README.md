# Social Network Analysis of the *Forrest Gump* Character Network

Group project for the Social Network Analysis course at LUISS University (academic year 2025/2026).

The project studies the network of character interactions in the movie *Forrest Gump* (nodes = characters, edges = shared scenes, weights = number of shared scenes) and applies the main tools of Social Network Analysis, from basic topology to diffusion models.

## What the project covers
- **Network topology**: 94 characters, 271 edges, density ≈ 0.062, average degree ≈ 5.77
- **Clustering**: manual implementation of the local clustering coefficient, validated against NetworkX; CCDF analysis of clustering and neighbor clustering
- **Centrality**: betweenness and closeness centrality to identify the key characters (Forrest, Jenny, Lt. Dan)
- **Community detection**: bridge removal vs. label propagation, compared through modularity (0.32 vs. 0.18); partition visualized in Gephi
- **Link prediction**: Common Neighbors and Jaccard Index, plus a combined normalized score
- **Network modelling**: preferential attachment with triadic closure, tuned to reproduce the real network's clustering
- **Diffusion**: random weighted fractional threshold model under different outbreak scenarios

## Repository structure
```text
├── notebook/notebook.ipynb         # full analysis, week by week
├── data/                           # nodes, edges and graph properties (CSV)
├── figures/                        # Gephi visualization and GEXF export of the communities
├── requirements.txt
└── README.md
```

## How to run
```bash
pip install -r requirements.txt
jupyter notebook notebook/notebook.ipynb
```
Run the notebook from the `notebook/` folder: it reads the data from `../data/`.

## Technologies
Python, NetworkX, pandas, NumPy, Matplotlib, Gephi, Jupyter Notebook

## Data
Character network from the Moviegalaxies dataset: J. Kaminski et al., "Moviegalaxies - Social Networks in Movies", Harvard Dataverse, V3 (2018). https://doi.org/10.7910/DVN/T4HBA3
