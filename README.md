# Code and data sources accompanying [Sun and Stephens (2018)][]

This repository contains code and data sources accompanying [Sun and Stephens (2018)][], which develops `cashr` methods to solve the Empirical Bayes Normal Means (EBNM) problem with correlated noise. The methods are implemented in the [`cashr`](https://github.com/LSun/cashr) package. See [the accompanion website for the paper][https://lsun.github.io/cashr_paper/] for more details.

Citing this work
----------------

If you find any of the code or other resources in this repository useful for your work, please cite our paper:

> Lei Sun and Matthew Stephens. (2018). "Solving the Empirical Bayes Normal Means Problem with Correlated Noise."

License
-------

Copyright (c) 2018, [Lei Sun][], [Matthew Stephens][]

All source code and software in this repository are made available under the terms of the [GNU General Public License](http://www.gnu.org/licenses/gpl.html). See the [LICENSE](LICENSE) file for the full text of the license.

Instruction
------------

You need to install the appropriate R packages and download this repository to your computer.

### Install software and R packages

1.  Install [`R`](https://cran.r-project.org).
2.  Install [`RStudio`](https://www.rstudio.com/).
3.  Install the required `R` packages by running the following commands in the `R` interactive environment. (Note the order of these commands is important---the Bioconductor packages should be installed before the CRAN packages.)
``` r
source("https://bioconductor.org/biocLite.R")
biocLite(c("qvalue", "limma", "edgeR"), suppressUpdates = TRUE)
install.packages(c("devtools", "ashr", "locfdr", "deconvolveR", "EbayesThresh",
                   "ggplot2", "reshape2", "scales", "gridExtra", "grid", "latex2exp"))
```
4. Install the `R` package `Rmosek` following the online instructions such as
- https://docs.mosek.com/8.1/rmosek/install-interface.html
- https://gist.github.com/mikelove/67ea44d5be5a053e599257fe357483dc
- https://rdrr.io/cran/ashr/f/inst/rmosek-mac.md
5. Once `Rmosek` is intalled, install additional `R` packages by running the following commands in the `R` interactive environment.
``` r
install.packages("REBayes")
devtools::install_github("LSun/cashr")
```

Data
----

1. The RNA-seq data set used for realistic simulations in this paper was created from the real human liver tissue RNA-seq gene expression read counts. In particular, the sample and gene identifiers have been removed from the data.

    The RNA-seq gene expression data were originally generated by the GTEx Project, which was supported by the Common Fund of the Office of the Director of the National Institutes of Health, and by NCI, NHGRI, NHLBI, NIDA, NIMH, and NINDS. The data used for the analyses described in this paper were obtained from the GTEx Portal at [the GTEx Portal](https://www.gtexportal.org).

2. The leukemia data set analyzed in this paper is maintained by [Bradley Efron][] and [Trevor Hastie][] at Stanford. The data set is available at http://statweb.stanford.edu/~ckirby/brad/LSI/datasets-and-programs/datasets.html and https://web.stanford.edu/~hastie/CASI/data.html.

3. The mouse data set analyzed in this paper was generated by Scott Adrian Smemo (RIP) and [Marcelo Nobrega][] at the University of Chicago.

4. The data are either stored in the `data/` directory or can be produced by the code provided in this repository.

-------------

This project is created with [workflowr][]. Special thanks to [David Gerard][], [Peter Carbonetto][], [John Blischak][]. If you find a bug, please create an [issue](https://github.com/LSun/cashr_paper/issues).

[Sun and Stephens (2018)]: https://arxiv.org/abs/1812.07488
[Lei Sun]: https://github.com/LSun
[Matthew Stephens]: http://stephenslab.uchicago.edu/
[Bradley Efron]: http://statweb.stanford.edu/~ckirby/brad/
[Trevor Hastie]: https://web.stanford.edu/~hastie/
[Marcelo Nobrega]: http://nobregalab.uchicago.edu/
[David Gerard]: https://dcgerard.github.io/
[Peter Carbonetto]: https://pcarbo.github.io/
[John Blischak]: https://jdblischak.com/
[workflowr]: https://github.com/jdblischak/workflowr
