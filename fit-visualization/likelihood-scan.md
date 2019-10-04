# Likelihood scan

## User story
As an analyzer, I want to visualize a test statistic distribution around its minimum, so that I can spot potential issues in the definition of the likelihood and present my fit result.

### Assumptions
- The distribution is supplied in a well-defined format.

### Acceptance criteria
- The test statistic distribution is visualized, and can be intersected with horizontal lines to show confidence intervals.
- Multiple distributions can be shown on the same figure.

## Example implementation
<img src="figures/likelihood-scan.png" alt="description" width="350"/>

Reference: [CERN-EP-2019-097, submitted to Phys. Rev. D](https://inspirehep.net/record/1752936)

The distribution of -2 ln Λ, based on profile likelihood ratio Λ, is shown as a function of a cross-section σ.
Multiple lines visualize the distribution when considering all or only some sources of uncertainty.
The horizontal lines intersecting with the distributions visualize the 1σ and 2σ confidence intervals.