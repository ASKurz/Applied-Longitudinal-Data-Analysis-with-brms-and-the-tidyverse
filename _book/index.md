--- 
title: "*Applied longitudinal data analysis* in brms and the tidyverse"
subtitle: "version 0.0.2"
author: "A Solomon Kurz"
date: "2021-04-06"
site: bookdown::bookdown_site
output: 
  bookdown::gitbook:
    split_bib: yes
documentclass: book
bibliography: bib.bib
biblio-style: apalike
csl: apa.csl
link-citations: yes
geometry:
  margin = 0.5in
urlcolor: blue
highlight: tango
header-includes:
  \usepackage{underscore}
  \usepackage[T1]{fontenc}
github-repo: ASKurz/Applied-Longitudinal-Data-Analysis-with-brms-and-the-tidyverse
twitter-handle: SolomonKurz
description: "This project is a reworking of Singer and Willett's classic (2003) text within a contemporary Bayesian framework with emphasis of the brms and tidyverse packages within the R computational framework."
---

# What and why {-}

This project is based on Singer and Willett's classic [-@singerAppliedLongitudinalData2003] text, [*Applied longitudinal data analysis: Modeling change and event occurrence*](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780195152968.001.0001/acprof-9780195152968). You can download the data used in the text at [http://www.bristol.ac.uk/cmm/learning/support/singer-willett.html](https://www.bristol.ac.uk/cmm/learning/support/singer-willett.html) and find a wealth of ideas on how to fit the models in the text at [https://stats.idre.ucla.edu/other/examples/alda/](https://stats.idre.ucla.edu/other/examples/alda/). My contributions show how to fit these models and others like them within a Bayesian framework. I make extensive use of Paul Bürkner's [**brms** package](https://github.com/paul-buerkner/brms) [@R-brms; @burknerBrmsPackageBayesian2017; @burknerAdvancedBayesianMultilevel2018], which makes it easy to fit Bayesian regression models in **R** [@R-base] using Hamiltonian Monte Carlo (HMC) via the [Stan](https://mc-stan.org) probabilistic programming language [@carpenterStanProbabilisticProgramming2017]. Much of the data wrangling and plotting code is done with packages connected to the [**tidyverse**](http://style.tidyverse.org) [@R-tidyverse; @wickhamWelcomeTidyverse2019].

## Caution: Work in progress {-}

This release contains drafts of Chapters 1 through 6 and 9 through 13. Chapters 1 through 6 provide the motivation and foundational principles for fitting longitudinal multilevel models. Chapters 9 through 13 motivation and foundational principles for fitting discrete-time survival analyses.

In addition to fleshing out more of the chapters, I plan to add more goodies like introductions to multivariate longitudinal models and mixed-effect location and scale models. But there is no time-table for this project. To keep up with the latest changes, check in at the GitHub repository, [https://github.com/ASKurz/Applied-Longitudinal-Data-Analysis-with-brms-and-the-tidyverse](https://github.com/ASKurz/Applied-Longitudinal-Data-Analysis-with-brms-and-the-tidyverse), or follow my announcements on twitter at [https://twitter.com/SolomonKurz](https://twitter.com/SolomonKurz).

## **R** setup {-}

To get the full benefit from this ebook, you'll need some software. Happily, everything will be free (provided you have access to a decent personal computer and an good internet connection).

First, you'll need to install **R**, which you can learn about at [https://cran.r-project.org/](https://cran.r-project.org/).

Though not necessary, your **R** experience might be more enjoyable if done through the free RStudio interface, which you can learn about at [https://rstudio.com/products/rstudio/](https://rstudio.com/products/rstudio/).

Once you have installed **R**, execute the following to install the bulk of the add-on packages. This will probably take a few minutes to finish. Go make yourself a coffee.


```r
packages <- c("bayesplot", "brms", "broom", "devtools", "flextable", "GGally", "ggmcmc", "ggrepel", "gtools", "loo", "patchwork", "psych", "Rcpp", "remotes", "rstan", "StanHeaders", "survival", "tidybayes", "tidyverse")

install.packages(packages, dependencies = T)
```

A few of the other packages are not officially available via the Comprehensive R Archive Network (CRAN; https://cran.r-project.org/). You can download them directly from GitHub by executing the following.


```r
devtools::install_github("stan-dev/cmdstanr")
remotes::install_github("stan-dev/posterior")
devtools::install_github("rmcelreath/rethinking")
```

It's possible you'll have problems installing some of these packages. Here are some likely suspects and where you can find help:

* for difficulties installing **brms**, go to [https://github.com/paul-buerkner/brms#how-do-i-install-brms](https://github.com/paul-buerkner/brms#how-do-i-install-brms) or search around in the [**brms** section of the Stan forums ](https://discourse.mc-stan.org/c/interfaces/brms/36);
* for difficulties installing **cmdstanr**, go to [https://mc-stan.org/cmdstanr/articles/cmdstanr.html](https://mc-stan.org/cmdstanr/articles/cmdstanr.html);
* for difficulties installing **rethinking**, go to [https://github.com/rmcelreath/rethinking#quick-installation](https://github.com/rmcelreath/rethinking#quick-installation); and
* for difficulties installing **rstan**, go to [https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started](https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started).

## License and citation {-}

This book is licensed under the Creative Commons Zero v1.0 Universal license. You can learn the details, [here](https://github.com/ASKurz/Applied-Longitudinal-Data-Analysis-with-brms-and-the-tidyverse/blob/master/LICENSE). In short, you can use my work. Just please give me the appropriate credit the same way you would for any other scholarly resource. Here's the citation information:


```r
@book{kurzAppliedLongitudinalDataAnalysis2021,
  title = {Applied longitudinal data analysis in brms and the tidyverse},
  author = {Kurz, A. Solomon},
  year = {2021},
  month = {4},
  edition = {version 0.0.2},
  url = {https://bookdown.org/content/4253/}
}
```

