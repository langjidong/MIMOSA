# MIMOSA
Model-based Integration of Metabolite Observations and Species Abundances

A pipeline for joint metabolic model-based analysis of metabolomics measurements and taxonomic composition from microbial communities. Includes an R package that implements the core integrative analysis functions as well as example pre-processing and analysis scripts. MIMOSA is under active development. See http://elbo.gs.washington.edu/download.html for a previous version of the code, used to produce the results in (Noecker et al, 2016).

## Contents

- **mimosa**: An R package to generate community-specific metabolic network model, use the model to make metabolite predictions and identify consistent and contrasting metabolite variation, identify potential taxonomic contributors to metabolite variation, and shuffle the community metabolic network for comparison of results with a null model. Some functions require the file `reaction_mapformula.lst` from the KEGG database (Kanehisa and Goto, 2000). If you do not have access to this file, you can email `elbo [at] uw.edu` for access to an older version.

You can install **mimosa** using the `devtools` package in R:
```R
devtools::install_github("borenstein-lab/MIMOSA/mimosa")
```

- **runMimosa.R**: wrapper script, used to run main MIMOSA analyses from the command line using `Rscript` with various options.

- **run_all.sh**: example script using `runMimosa.R` to regenerate results from one of the datasets described in Noecker et al, 2016. This script uses the Python modules [`picrust`](http://picrust.github.io/picrust/)(Langille et al, 2013) and [`MUSiCC`](http://elbo.gs.washington.edu/software_musicc.html)(Manor and Borenstein, 2015) to process and prepare the datasets. 

## Citation

Noecker, C., Eng, A., Srinivasan, S., Theriot, C.M., Young, V.B., Jansson, J.K., Fredricks, D.N., and Borenstein, E. (2016). Metabolic Model-Based Integration of Microbiome Taxonomic and Metabolomic Profiles Elucidates Mechanistic Links between Ecological and Metabolic Variation. mSystems 1, e00013–15, doi:[10.1128/mSystems.00013-15](http://msystems.asm.org/content/1/1/e00013-15).
