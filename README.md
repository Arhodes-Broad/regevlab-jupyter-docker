# Jupyter Docker Image with single-cell R/Python packages
# Test 1

## Base image
* [debian:stretch](https://hub.docker.com/r/library/debian/)

## Applications
* [Jupyter Notebooks](https://jupyter-notebook.readthedocs.io/en/stable/)
* [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/)
* [Hail 0.2](https://hail.is/docs/0.2/index.html)

## Kernels
* Python 2.7
* Python 3.6
* R 3.5

## Libraries
Warning: may be incomplete! Consult the Dockerfile for the source of truth.
* common
   * google-cloud-sdk
   * Unix utilities
* python
   * google-cloud-*
   * numpy
   * pandas
   * seaborn
   * firecloud-api
   * scikit-learn
   * statsmodels
   * ggplot
   * bokeh
   * pyfasta
   * pdoc
   * biopython
   * bx-python
   * fastinterval
   * matplotlib-venn
   * scanpy
* R
   * evaluate
   * pbdZMQ
   * devtools
   * uuid
   * reshape2
   * bigrquery
   * googleCloudStorageR
   * tidyverse
   * DataBiosphere/Ronaldo
   * Bioconductor core packages
   * Seurat v3 / scran / scater
    
## Extensions
* jupyter_localize_extension.py
   * Server-side extension to provide the `/localize` endpoint to localize/delocalize files between
     GCS and the Leo cluster.
* jupyter_delocalize.py
   * Provides a custom Jupyter [ContentsManager](https://jupyter-notebook.readthedocs.io/en/stable/extending/contents.html)
     which persists notebooks to a configurable GCS location upon save.
* google_sign_in.js
   * Front-end extension which keeps the user signed into Google while using a notebook.
