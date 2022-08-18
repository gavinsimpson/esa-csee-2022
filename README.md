# ESA & CSEE Joint Annual Meeting Talk 2022

## Quantifying trends in biodiversity with generalized additive models

### Gavin Simpson

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7003948.svg)](https://doi.org/10.5281/zenodo.7003948)

Slides & related R code for a talk that gave at the join ESA & CSEE annual
meeting in Montreal, Canada, August 18, 2022.

Rendered slidedeck: https://gavinsimpson.github.io/esa-csee-2022/

#### Abstract

##### Background/Question/Methods

Climate change and other human-caused environmental disturbance may lead to
declines in biodiversity. Recently, a number of studies have collated large data
sets of monitoring time series for selected ecosystem or organism groups and
used these data sets to estimate trends in biodiversity, with many studies
identifying large declines in biodiversity across a number of organisms or
ecosystems. These results are not without controversy however; data selection
and quality issues, as well as questions over statistical methodology have lead
to vigorous debate.

Typically, trends in biodiversity are estimated using linear effects, via
generalized linear mixed (or hierarchical) models to account for site-to-site
heterogeneity in temporal trends. Additionally, year-to-year variation may
enhance or mask estimated losses or gains in biodiversity over time if the first
observation year in a given series is unusually rich or depauperate. Using year
random effects has been suggested as a mechanism to account for this potential
bias. An alternative way to model trends in biodiversity time series is using
penalized splines for the trends, leading to hierarchical generalized additive
models (HGAMs). Here, I introduce HGAMs and penalized splines and their use for
modelling biodiversity trends, and reanalyze a forest arthropod diversity time
series data set.

##### Results/Conclusions

HGAMs were fitted to the forest arthropod data (150 plots, 9 years per plot)
that included a variety of decompositions of biodiversity trends. Of the these,
two models had clearly superior predictive ability: (1) a model with
region-specific trends plus plot-specific random smooths (AIC 15120), and (2)
as model (1) plus year random effects to model the average year-to-year effects
(AIC 15122). Both models represent significant improvements over a GLMM with
linear trends plus random linear slopes per plot and year-to-year effects (AIC
15467). The main difference between the two HGAMs is the complexity of the
region-specific trends: model (2) had simpler regional trends, closer to linear,
than model (1), due to the additional year-to-year effect modelling variation
ascribed to the regional trends in model (1).

This shows that there may be several ways to decompose trends in biodiversity
data that are equally good at describing those underlying trends. Here, the bias
in the estimated linear trends due to many series starting in "good" years can
be removed either via the year-to-year random effect or region specific smooths,
both of which capture the overall tendency for some years to have greater
arthropod abundance than others.
