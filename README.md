# Commuting-Flow-Eigenanalysis
This project analyses commuting flows between UK MSOAs (Middle Layer Super Output Areas) using eigen decomposition and singular value techniques. It demonstrates how linear algebra (power iteration, SVD, eigenpairs) can reveal hidden structures in travel data.

🚀 Features
. Implements power iteration to find the dominant eigenpair of the OD matrix.
. Extends to multiple eigenvectors using a Gram–Schmidt projection (deflated power method).
. Computes eigenpairs of XᵀX (destination clustering) and XXᵀ (origin clustering) — effectively an SVD.
. Visualises eigenvectors as maps of MSOAs over a UK basemap.

📂 Data
. The full Origin–Destination Workplace matrix (ODWP_matrix.npy) from the 2021 UK Census is not included due to GitHub file size limits.

  Instead, this repo contains:
. The Python analysis code (ready to run if you provide your own OD matrix).
. An images/ folder with example screenshots of results from the full dataset.
. If you want to reproduce the full analysis, you can download the commuting flow data directly from the ONS Census datasets
  and save it as ODWP_matrix.npy and coords.npy

🛠️ Requirements
. Python 3.9+
. Libraries: numpy, pandas, matplotlib

🔬 Methods Explained
. Power iteration → finds the dominant commuting eigenmode.
. Deflated power method (Gram–Schmidt) → extracts multiple orthogonal eigenmodes.
. XtX and XXt eigenpairs → separate destination vs origin commuting clusters.
. Visualisation → eigenvectors are mapped onto MSOA coordinates to reveal regional patterns.
