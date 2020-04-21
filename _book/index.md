--- 
title: "*Applied Longitudinal Data Analysis* in brms and the tidyverse"
subtitle: "version 0.0.1"
author: ["A Solomon Kurz"]
date: "2020-04-21"
site: bookdown::bookdown_site
output: bookdown::gitbook
documentclass: book
geometry:
  margin = 0.5in
urlcolor: blue
highlight: tango
header-includes:
  \usepackage{underscore}
  \usepackage[T1]{fontenc}
link-citations: yes
github-repo: ASKurz/Applied-Longitudinal-Data-Analysis-with-brms-and-the-tidyverse
twitter-handle: SolomonKurz
description: "This project is a reworking of Singer and Willett's classic (2003) text within a contemporary Bayesian framework with emphasis of the brms and tidyverse packages within the R computational framework."
---

# What and why {-}

This project is based on Singer and Willett's classic (2003) text, [*Applied longitudinal data analysis: Modeling change and event occurrence*](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780195152968.001.0001/acprof-9780195152968). You can download the data used in the text at [http://www.bristol.ac.uk/cmm/learning/support/singer-willett.html](https://www.bristol.ac.uk/cmm/learning/support/singer-willett.html) and find a wealth of ideas on how to fit the models in the text at [https://stats.idre.ucla.edu/other/examples/alda/](https://stats.idre.ucla.edu/other/examples/alda/). My contributions show how to fit these models and others like them within a Bayesian framework. I make extensive use of Paul Bürkner's [**brms** package](https://github.com/paul-buerkner/brms), which makes it easy to fit Bayesian regression models in **R** using Hamiltonian Monte Carlo (HMC) via the [Stan](https://mc-stan.org) probabilistic programming language. Much of the data wrangling and plotting code is done with packages connected to the [**tidyverse**](https://www.tidyverse.org).

## Caution: Work in progress {-}

This inaugural 0.0.1 release contains first drafts of Chapters 1 through 5 and 9 through 12. Chapters 1 through 5 provide the motivation and foundational principles for fitting longitudinal multilevel models. Chapters 9 through 12 motivation and foundational principles for fitting discrete-time survival analyses. A few of the remaining chapters have partially completed drafts and will be added sometime soon.

In addition to fleshing out more of the chapters, I plan to add more goodies like introductions to multivariate longitudinal models and mixed-effect location and scale models. But there is no time-table for this project. To keep up with the latest changes, check in at the GitHub repository, [https://github.com/ASKurz/Applied-Longitudinal-Data-Analysis-with-brms-and-the-tidyverse](https://github.com/ASKurz/Applied-Longitudinal-Data-Analysis-with-brms-and-the-tidyverse), or follow my announcements on twitter at [https://twitter.com/SolomonKurz](https://twitter.com/SolomonKurz).

