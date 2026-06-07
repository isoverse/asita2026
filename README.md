# ASITA 2026

## Installation

1.  Download and install [R](https://cloud.r-project.org/) (should be >= 4.5)
2.  Download and install [RStudio](https://posit.co/download/rstudio-desktop) (more beginner friendly) or [Positron](https://positron.posit.co/download.html) (more powerful)
3.  If you are working on Windows, download and install Rtools (for the latest R version 4.5 and 4.6, use [RTools4.5](https://cran.r-project.org/bin/windows/Rtools/rtools45/rtools.html)) - note that this step won't be necessary anymore once [**isoreader2**](https://isoreader2.isoverse.org/) is available on CRAN
3.  Start RStudio/Positron
4.  in the **Console** at the bottom, copy the following commands and hit enter to execute them:

```r
# checks that you are set up to build R packages from source
if (!requireNamespace("pkgbuild", quietly = TRUE)) {
  install.packages("pkgbuild")
}
pkgbuild::check_build_tools()

# installs the latest isoreader2 package from GitHub
if (!requireNamespace("pak", quietly = TRUE)) {
  install.packages("pak")
}
pak::pak("isoverse/isoreader2")

# install isoexplorer
pak::pak("isoverse/isoexplorer")

# check/install isoextract
isoreader2::ir_check_isoextract()
```
