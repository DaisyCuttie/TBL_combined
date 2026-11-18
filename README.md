# TBL Spatial Combined Viewer

This folder contains a combined web viewer for these four Seurat spatial datasets
(`dataset` annotation layer in the viewer):

| Dataset | Sample | Source | Cells |
|---|---|---|---|
| `24.1` | Bovis1 | `TBL_Spatial_24.1_imputed.rds` | 333,788 |
| `24.2` | Bovis2 | `TBL_Spatial_24.2_imputed.rds` (FOV 1-27) | 84,666 |
| `24.3` | MTB1 | `TBL_Spatial_24.3_imputed.rds` (FOV 63-64) | 1,413 |
| `24.4` | MTB2 | `TBL_Spatial_24.4_imputed.rds` (FOV 65-95) | 63,258 |

Cells are coloured by `predicted_celltype` using the subtype palette from
`Spatial_Color.xlsx` (the same colours as the SpatialDimPlot figures). Gene
expression is the RNA assay `data` layer (measured, log-normalised).

## Contents

- `index.html`: web viewer
- `data/cells.json`: combined cell coordinates and labels
- `data/metadata.json`: dataset metadata
- `data/gene_list.json`: exported gene list
- `data/genes/`: per-gene expression files (sparse; `idx` stored as gaps between
  consecutive cell indices when `"delta": true`)
- `data/poly_coords.bin` and `data/poly_offsets.bin`: polygon geometry

## GitHub Pages
- https://daisycuttie.github.io/TBL_combined/
