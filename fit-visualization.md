# Fit visualization

This lists various kinds of visualizations for template fits, some of which are specifically aimed at profile likelihood fits.

## List of different types of visualizations
### Inputs to the fit
- [Pruning plot](fit-visualization/pruning-plot.md)
- [Nuisance parameter effects](fit-visualization/nuisance-parameter-effects.md)
### Fit results
- [Pull plot](fit-visualization/pull-plot.md)
- [Correlation matrix](fit-visualization/correlation-matrix.md)
- [Exclusion limits](fit-visualization/exclusion-limits.md)
- [Likelihood scan](fit-visualization/likelihood-scan.md)
- [Ranking plot](fit-visualization/ranking-plot.md)

Template: [template file](fit-visualization/template.md)


## General acceptance criteria
- The visualization can be adjusted to conform to formatting rules required by the users:
    - logos (e.g. of an experiment) can be included,
    - additional text can be added (e.g. center of mass energy and integrated luminosity for an LHC result).
- Colors used in the visualization avoid the common pitfalls listed in [Fundamentals of Data Visualization](https://serialmentor.com/dataviz/color-pitfalls.html), and are colorblind friendly as verified via a [cvd simulator](https://www.color-blindness.com/coblis-color-blindness-simulator/).
- All relevant information about the figure is retained when viewing it in grayscale.

## Relevant terms

### Parameter of interest (POI)
The parameter of interest (POI) is the parameter that a measurement aims to determine.
There can be more than one parameter of interest in a measurement.

### Nuisance parameter (NP)
A Nuisance parameter (NP) is not of direct interest in a measurement, but affects it and therefore must be accounted for.

### Impact
The impact of a nuisance parameter on a parameter of interest is defined as the shift ∆μ in the parameter of interest between the nominal fit and another fit where the nuisance parameter θ is held fixed at θ ± x.
The pre-fit impact of a nuisance parameter is obtained for x = ∆θ, where ∆θ is the uncertainty for this nuisance parameter as determined from a subsidiary measurement.
The post-fit impact is obtained when replacing ∆θ by the uncertainty for the nuisance parameter as determined in the measurement.

### Pull
The pull of a parameter is given by the difference between its nominal pre-fit value and its best-fit value as determined in the fit, and this difference is divided by the (pre-fit) uncertainty ∆θ as given by a subsidiary measurement.

### Pruning
Nuisance parameters can be removed from the fit if they have a negligible effect on it.
The procedure of removing them is called pruning.
Pruning can either completely or only partially remove the effect of a nuisance parameter.
In the high energy physics context, the effect of a nuisance parameter may for example be pruned for specific samples or channels.
The effects of a nuisance parameter on a distribution can also be split into a normalization and a shape effect, and these can be pruned independently.