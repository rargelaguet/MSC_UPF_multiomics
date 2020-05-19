
# Installation

There are two versions of MOFA. The first one is in Bioconductor (https://bioconductor.org/packages/release/bioc/html/MOFA.html), but it is now depreciated.
The second version, MOFA2, is still not available in Bioconductor, but it can be installed via its github repository: https://github.com/bioFAM/MOFA2#installation
The core of MOFA is implemented in Python, but we provide an R wrapper, which is what most people use.

## Python dependencies

Python dependencies can be installed from the unix terminal using pip:
```r
pip install mofapy2
```


## R package
Can be installed from R (after installing the [mofapy2](https://pypi.org/project/mofapy2/) package):

```r
MOFA2 R package can be installed using:
	remotes::install_github("bioFAM/MOFA2/MOFA2", build_opts = c("--no-resave-data --no-build-vignettes"))
```

## Reticulate
MOFA requires [reticulate](https://rstudio.github.io/reticulate/) to communicate with Python, and this is the source of most of the installation problems.
If you have multiple python versions installed you need to keep track of which one you used to install the `mofapy2` package. Then, run **at the start of your R session**:

```r
library(reticulate)
use_python("YOUR_PYTHON_PATH", required=TRUE)
```

## Data sets for vignettes
The data for the CLL vignette that we will go throuhg can be accessed from the [MOFAdata](https://www.bioconductor.org/packages/release/data/experiment/html/MOFAdata.html) package. This can be installed from R as follows:

```r
BiocManager::install("MOFAdata")
```


# Vignettes

If you are interested in following up with MOFA, we provide a variety of [vignettes](https://github.com/bioFAM/MOFA2#tutorialsvignettes), including real case examples.


# FAQ

For general questions you can read the [FAQ section](https://github.com/bioFAM/MOFA2#frequently-asked-questions-faq)

