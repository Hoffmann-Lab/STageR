## STageR

STage of aging estimatoR: Cluster-based epigenetic clockwise classifier predicting the aging stage

# How to clone the repository

`git clone https://github.com/Hoffmann-Lab/STageR`

# Requirements

The code was run using `R` version 4.2.2 (2022-10-31) but will very likely work with other versions of `R`.
The following libraries has to be installed (the version used for our run is stated in the brackets): `glmnet` (v4.1-7), `dplyr` (v1.1.2), `tidyverse` (v2.0.0) , `tibble` (v3.2.1), `ComplexHeatmap` (v2.14.0), `ggplot2` (v3.4.2).


# How to run the scripts

`STageR.predict.Rmd` predicts the epigenetic aging stage of mouse (early life, midlife, late life) based on DNA methylation in intestine. It reads the validation data from Olecka & van Boemmel et al. (2023) to show the prediction of the aging stages for 20 samples. The predicted probabilities are visualised using a barplot. The confusion matrix summarizing all samples in the validation set is also shown. `STageR.predict.Rmd` runs only few seconds on a standard machine.

You may knit the `STageR.predict.Rmd` directly in the RStudio or run 
`Rscript -e "rmarkdown::render('STageR.predict.Rmd')"` on the command line.

If you want to run the training of the algorithms and calculate the results from the cross validation, run the `STageR.training.Rmd`. It reads the matrix with methylation values in the CpGs overlapping the clusters, then estimates the final model using all samples and run the cross validation procedure. It plots the distribution of the estimated coefficients, confusion matrix and the model matrix. `STageR.training.Rmd` with 10 repetition of the 10-fold CV runs few minutes on a standard machine.

You can knit the `STageR.training.Rmd` directly in the RStudio or run 
`Rscript -e "rmarkdown::render('STageR.training.Rmd')"` on the command line.


