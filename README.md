# ASITA 2026

## Installation

1. Download and install [R](https://cloud.r-project.org/) (should be >= 4.5)
1. Download and install [RStudio](https://posit.co/download/rstudio-desktop) (more beginner friendly) or [Positron](https://positron.posit.co/download.html) (more powerful)
1. If you are working on Windows, download and install Rtools (for the latest R version 4.5 and 4.6, use [RTools4.5](https://cran.r-project.org/bin/windows/Rtools/rtools45/rtools.html)) - note that this step won't be necessary anymore once [**isoreader2**](https://isoreader2.isoverse.org/) is available on CRAN
1. Download and unzip this [workshop folder](https://github.com/isoverse/asita2026/archive/refs/heads/main.zip) on your computer
1. Start RStudio or Positron
1. Open the workshop folder project: in Rstudio `File` -> `Open project`, in Positron `File` -> `Open folder` and navigate to the downloaded `asita2026-main` folder
1. In the **Console** at the bottom, copy the following commands and hit enter to execute them:

```r
# checks that you are set up to build R packages from source
install.packages("pkgbuild")
pkgbuild::check_build_tools()

# installs the latest isoreader2 package from GitHub
install.packages("pak")
pak::pak("isoverse/isoreader2")

# install isoexplorer
pak::pak("isoverse/isoexplorer")

# check/install isoextract
isoreader2::ir_check_isoextract()
```

If everything worked, the last line of these commands should have returned `isoreader2::ir_check_isoextract() found isoextract version 0.2.0.0 ready for use`. If yes, congrats! You're ready for following along during the coding portion the workshop! If no, try to run these commands one line at a time to see where there's trouble.
