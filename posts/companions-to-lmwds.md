<!--
.. title: The mass distribution of companions to low-mass white dwarfs
.. slug: mass-distribution-lmwds
.. date: 2014-12-01 09:30:00 UTC-05:00
.. tags: hacking, statistics, paper
.. author: Adrian Price-Whelan
.. link:
.. description: Inferring the mass distribution of companion to single-line, spectroscopic binary stars
.. type: text
-->

<div style="float:left">
<img src="/images/LMWD-fig.jpg" width="300px">
<br>
<small><a href="http://arxiv.org/pdf/1412.0114.pdf">(see Figure 4)</a></small>
</div>

I came to Astro Hack Week with a statistics-heavy project that was quite different from my usual research interests (I mainly work on Galactic dynamics). I was very surprised that a few weeks after arriving home, we had a submitted paper, and even more surprised that a few days after that, a very favorable referee report! The paper is now accepted to ApJL, and [posted to the arXiv](http://arxiv.org/pdf/1412.0114.pdf).

** Introduction **
The universe isn't old enough to produce low-mass White Dwarfs (LMWDs; WDs with masses < 0.4 $M_\odot$) through single-star evolution. These stars are thought to have been formed in tight binary systems where the companion star is close enough to strip matter from the envelope of the primary star as it evolves through the red giant phase. Many LMWDs are known (thanks to SDSS and follow-up from the ELM survey) and most of them show radial velocity oscillations with timescales typically around ~0.5 day, suggesting that these stars are in binary systems. Binary stars are extremely useful for studying stellar evolution and constraining stellar evolution models because, with orbital modeling, the masses of the stars can be determined to high accuracy. However, these stars show no directly-detectable companions -- in optical light, these stars do not contribute appreciably to photometry or spectra, and radio follow-up of a handful of the companions yielded all non-detections. This is further complicated by the fact that the binaries in this sample seem to be decoupled, thus, the inclination angle of the orbit relative to the observer is unknown and cannot be solved for by, for example, ellipsoidal variation of the light curve.

Not knowning the inclination angle means, for a single system, we can only place a lower-limit on the mass of the companion star, but the data still contain useful information about the mass distribution of the unseen companion stars! If the inclination angles are isotropically distributed, as we would expect, then we can still constrain properties of the mass distribution of the companion stars.

<!-- TEASER_END -->

** The Model **
Most of the companion stars are likely to be more massive WDs (remember, WDs are weird and the more massive stars can contract more, meaning they are fainter). One of the main goals of this project is to constrain the fraction of these systems that could contain Neutron Star (NS) companions. NS's in binaries are very interesting objects as X-ray and radio follow-up could allow for a precise measurement of the NS mass to compare with NS structure models (only a handful of NS's have measured masses). We therefore choose to represent the companion mass distribution as a two-component Gaussian, where each component is truncated at physically motivated bounds. The lower-mass component represents a WD companion population (WD-WD binaries), and is truncated (at the upper end) at the Chandrasekhar mass (1.44 $M_\odot$). The high-mass component represents the NS companions (WD-NS binaries) and is fixed to be a tight ($\sigma = 0.05$) distribution centered on 1.4 $M_\odot$. This distribution is truncated at the lower end at 1.3 $M_\odot$, thought to be the lowest possible mass of a NS.

** Results **
We apply this model to a number of mock data sets, a set of real data (Main Sequence - White Dwarf binaries) where the companion masses are known, and finally, to a sample of 55 single-line, spectroscopic binary LMWDs. Read about the tests in [the paper](http://arxiv.org/pdf/1412.0114.pdf).

Our results from applying to the LMWD binaries are consistent with having a 0% NS fraction, however the inferred NS fraction has an appreciable tail up to ~15% (see above figure). Many more LMWDs are being followed up with ground-based spectroscopic campaigns, and with future data sets we will be able to better constrain the NS fraction, as well as properties of the companion WD population.

This work was done in collaboration with [Jeff Andrews](http://user.astro.columbia.edu/~andrews/), and came about thanks to  useful conversations with [David Hogg](http://cosmo.nyu.edu/hogg/) and [DF-M](http://dfm.io) at the Astro Hack Week!
