# CMS Higgs to four leptons example

We will use this CMS Open Data Example ([http://opendata.cern.ch/record/5500 ](http://opendata.cern.ch/record/5500) )
as the reference implementation defining this analysis use case. 

```
Higgs-to-four-lepton analysis example using 2011-2012 data
Jomhari, Nur Zulaiha; Geiser, Achim; Bin Anuar, Afiq Aizuddin;

Cite as: Jomhari, Nur Zulaiha; Geiser, Achim; Bin Anuar, Afiq Aizuddin; (2017). Higgs-to-four-lepton analysis example using 2011-2012 data. CERN Open Data Portal. DOI:10.7483/OPENDATA.CMS.JKB8.RR42
```

## Excerpt from Open Data page

The published reference plot which is being approximated in this example is https://inspirehep.net/record/1124338/files/H4l_mass_3.png. Other Higgs final states (e.g. Higgs to two photons), which were also part of the same CMS paper and strongly contributed to the Higgs boson discovery, are not covered by this example.

![Mass plot](https://inspirehep.net/record/1124338/files/H4l_mass_v3.png)

The example consists of different levels of complexity. The highest level of this example addresses users who feel they have at least some minimal understanding of the content of this paper and of the meaning of this reference plot, which can be reached via (separate) educational exercises. The lower levels might also be interesting for educational applications. The example requires a minimal acquaintance with the linux operating system and the ROOT analysis tool.

The example uses legacy versions of the original CMS data sets in the CMS AOD, which slightly differ from the ones used for the publication due to improved calibrations. It also uses legacy versions of the corresponding Monte Carlo simulations, which are again close to, but not identical to, the ones in the original publication. These legacy data and MC sets listed below were used in practice, exactly as they are, in many later CMS publications.

Since according to the CMS Open Data policy the fraction of data which are public (and used here) is only 50% of the available LHC Run I samples, the statistical significance is reduced with respect to what can be achieved with the full dataset. However, the original paper Phys.Lett. B716 (2012) 30-61, arXiv:1207.7235, was also obtained with only part of the Run I statistics, roughly equivalent to the luminosity of the public sets, but with only partial statistical overlap.

The provided analysis code recodes the spirit of the original analysis and recodes many of the original cuts on original data objects, but does not provide the original analysis code itself. Also, for the sake of simplicity, it skips some of the more advanced analysis methods of the original paper. Nevertheless, it provides a qualitative insight about how the original result was obtained. In addition to the documented core results, the resulting root files also contain many undocumented plots which grew as a side product from setting up this example and earlier examples. The significance of the Higgs 'excess' is about 2 standard deviations in this example, while it was 3.2 standard deviations in this channel alone in the original publication. The difference is attributed to the less sophisticated background suppression. In more recent (not yet public) CMS data sets with higher statistics the signal is observed in a preliminary analysis with more than 5 standard deviations in this channel alone CMS-PAS-HIG-16-041.

The analysis strategy is the following: Get the 4mu and 2mu2e final states from the DoubleMuParked datasets and the 4e final state from the DoubleElectron dataset. This avoids double counting due to trigger overlaps. All MC contributions except top use data-driven normalization: The DY (Z/gamma^*) contribution is scaled to the Z peak. The ZZ contribution is scaled to describe the data in the independent mass range 180-600 GeV. The Higgs contribution is scaled to describe the data in the signal region. The (very small) top contribution remains scaled to the MC generator cross section.


## The demo running on cloud-native infrastructure

See blog post: http://cylindricalonion.web.cern.ch/blog/201906/finding-higgs-boson-within-minutes-cloud

The code: https://github.com/lukasheinrich/higgs-demo 
