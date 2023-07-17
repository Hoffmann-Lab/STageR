# STageR
STage of aging estimatoR: Cluster-based epigenetic clockwise classifier predicting the aging stage

`STageR.predict.Rmd` predicts the aging stage of mouse (early life, midlife, late life) based on DNA methylation in intestine. It reads the validation data from Olecka & van Boemmel et al. (2023) to show the prediction of the aging stages for 20 samples. The predicted probabilities are visualised using a barplot. The confusion matrix summarizing all samples in the validation set is also shown.

You can knit the `STageR.predict.Rmd` directly in the RStudio or run 
`Rscript -e "rmarkdown::render('STageR.predict.Rmd')"` on the command line.

