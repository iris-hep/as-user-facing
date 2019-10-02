## Ranking plot

### User story
As an analyser, I want to see which nuisance parameters contribute most to the uncertainty on the parameter(s) of interest that I am measuring. This is done so I can understand what limits the precision of my measurement, and which aspects of the statistical analysis should receive the most scrutiny.

#### Assumptions
- The evaluation of the _impact_ of each nuisance parameter is defined.
- The _impact_ per nuisance parameter is calculated and provided in a well-defined format.
- If the nuisance parameter _pulls_ are also shown, they are provided in a well-defined format (see also the section on pull plots, [needs link](link))
- For measurements with more than one parameter of interest, there is either a way to show the _impact_ with respect to every parameter of interest, or a way to combine it into a single quantity for multiple parameters of interest.

#### Acceptance criteria
- When ranking nuisance parameters in profile likelihood fits, both the pre- and the post-fit impact of each nuisance parameter is defined.
- If the pre-fit impact is not defined (for example for free-floating nuisance parameters), there is a way to either define the pre-fit uncertainty for this nuisance parameter, or a way to exclude it from the visualization.

### Example implementation
Reference: [Phys.Rev. D97 (2018) no.7, 072016
](https://doi.org/10.1103/PhysRevD.97.072016)

![ranking plot](fit-diagnostics/ranking_plot.png "ranking plot")