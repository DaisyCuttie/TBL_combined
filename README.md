# TBL Spatial Combined Viewer

This folder contains a combined web viewer for these three Seurat spatial datasets:

- `TBL_Spatial_24.1_imputed.rds`
- `TBL_Spatial_24.2_imputed.rds`
- `TBL_Spatial_24.4_imputed.rds`

## Contents

- `index.html`: web viewer
- `data/cells.json`: combined cell coordinates and labels
- `data/metadata.json`: dataset metadata
- `data/gene_list.json`: exported gene list
- `data/genes/`: per-gene expression files
- `data/poly_coords.bin` and `data/poly_offsets.bin`: polygon geometry

## Local test

Run a local web server from this folder:

```bash
cd /Users/chanyue/Desktop/Chauoki/TBL_Spatial/output/TBL_Spatial_combined
python3 -m http.server 8000
```

Then open:

- [http://localhost:8000/index.html](http://localhost:8000/index.html)

## GitHub Pages

Upload the contents of this folder to the root of a GitHub repository, then enable:

- `Settings` -> `Pages`
- `Deploy from a branch`
- Branch: `main`
- Folder: `/(root)`

## Notes

- This combined viewer includes all 3 datasets in one space.
- The exported data is large, about `1.2G`.
- `metadata.json` includes a `dataset` annotation layer so the three source datasets can be separated in the viewer.
