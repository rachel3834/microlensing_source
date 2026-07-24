---
title: "Blending"
permalink: /theory/blending/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
Continuing to explore complications which can cause microlensing events to deviate from purely PSPL models, we will now look at a
more data-orientated issue which is nevertheless related to parallax because it's affects can mimic a parallax signature; the two
are degenerate and need to be considered carefully. This issue is blending.

## Blending
Assumption No. 2: That the image of the lensed source in our CCD frames is always isolated and the flux from it can always be
measured independently from all neighboring stars.

<figure>
  <img src="{{ '/assets/images/OGLE-2012-BLG-0406_1.png' | relative_url }}" alt="Image of a dense starfield in the Galactic bulge" width="200">
  <figcaption>The field of OGLE-2012-BLG-0406 (centered) imaged by one of LCO's 2m telescopes, showing the high density of stars typical in microlensing observations.[Y.Tsapras]</figcaption>
</figure>

Microlensing is an intrinsically rare phenomenon, due to the precise alignment required between observer, lens and source. To
detect these events in significant numbers, all surveys to date have concentrated their observations in very dense starfields such
as the Galactic Bulge and Magallenic Clouds. The resulting CCD images are very crowded and its rare to have star which is entirely
isolated from its neighbors.
Although we don't resolve the disk of the stars in these observations - they remain points of light - the light from each star
in the frame is spread over a circle of pixels due to diffraction at the telescope aperture. This shape of this circle is described
by the star's Point Spread Function (PSF), which will have a certain Full Width Half Maximum (FWHM) depending on the telescope
 and seeing conditions at the time. The instrument detects the light via an array of pixels, each of which subtends an angle on sky
(the pixel scale) which is specific to that camera and telescope.  If the PSFs of neighboring stars overlap, they are said to be blended. These neighbors
are probably not physically associated with the target; they could be at any distance, but lie at a close angular separation from our line
of sight.

<figure>
  <img src="{{ '/assets/images/blending_schematic.png' | relative_url }}" alt="Illustration of blended star images." width="200">
  <figcaption>The light from multiple distinct stars is often blended together in our images, but only the flux from one of them exhibits a lensing lightcurve when measured as a function of time.[R.A.Street]</figcaption>
</figure>

## Affects of Blending<
Blending results in light from the neighbors contaminating the flux measurement of the lensed star, f<sub>s</sub>. Whereas for
an isolated lensed star, the flux at a given time t, f(t) is given by:
<table width="75%"><tr><td>$$f(t) = f_{s}(t)A(u(t))$$</td><td>[29]</td></tr></table>
in practise what we actually measure is more like:

<table width="75%"><tr><td>$$f(t) = f_{s}(t)A(u(t)) + f_{b}$$</td><td>[30]</td></tr></table>

where f<sub>b</sub>(t) is the additional flux from all overlapping neighbors. This is heavily time-dependant: for instance, if
the seeing suddenly worsens during observations, the PSF FWHM expands and f<sub>b</sub> abruptly increases.

<figure>
  <img src="{{ '/assets/images/blending_lightcurve_schematic.png' | relative_url }}" alt="Illustration of the effects of blending on a microlensing lightcurve" width="200">
  <figcaption>The solid black lightcurve shows an unblended lensing event in comparison with the dotted blue lightcurve where the lensed star is blended.[R.A.Street]</figcaption>
</figure>

The figure above shows the affect of blending on a microlensing event. Overall, the additional flux can "dilute" the measured amplitude,
and make t<sub>E</sub> appear shorter, leading to a mis-estimation of the lens parameters.  As this can be a symmetrical change in
the lightcurve, it can mimic the affects of the parallax component &pi;<sub>E,&perp;</sub>.

## Dealing with Blending
Multiple sets of observations from different instruments can help here. As each one may come from telescopes of very different
aperture, f<sub>s</sub>, even unblended, will still differ between datasets just as f<sub>b</sub>, so we consider both as functions
of time for each dataset, k (with N<sub>k</sub> datapoints), in turn:

<table width="75%"><tr><td>$$f_{k}(t) = f_{s,k}(t)A(u(t)) + f_{b,k}$$</td><td>[31]</td></tr></table>

Of course, they’re all observing the same event, so A(u(t)) relates the datasets together.
We begin by adopting initial typical values for the physical event parameters, to derive a starting model A(u(t)).
Eqn. 31 gives us a model for the flux measured from each dataset, f<sub>m,k</sub>(t), with measurement errors, σ<sub>m,k</sub>(t).
We can test how well the model fits with a &chi;<sup>2</sup> test:

<table width="75%"><tr><td>$$\chi^{2} = \frac{\sum_{i} \left( \frac{f_{m,k}(t) - f_{k}(t)}{\sigma_{m,k}(t)} \right)^{2}}{N_{k} - N_{par}}$$</td><td>[32]</td></tr></table>

where Npar is the number of fitted parameters.
Differentiating this expression with respect to each variable in turn and equating it to zero, we can derive a set of
simultaneous equations which can be used to infer f<sub>s,k</sub>, f<sub>b,k</sub> for each dataset, for the given amplification
model.

Given this set of initial blending parameters, we can now repeat this process, but this time fit for the physical parameters of
the amplification model. By iterating this process, we can arrive a set of consistent parameters for both models.

## Stellar variability
So far we have assumed that the blended neighbors to the lensed star 
give constant flux over the duration of the lensing event.  Of course, 
that isn't always the case, and if one or more neighboring stars has
intrinsic variability, f<sub>b</sub> may also vary with time.  This 
can be accommodated in the modeling of microlensing events by 
replacing f<sub>b</sub> in the iterative process above by introducing 
a f<sub>b</sub>(t) equal to an appropriate function, for instance a 
linear gradient or sinusoid (for example Street et al. 2013).  
Observations taken before or after the lensing event can be used to 
determine a suitable model.

## References
[Alcock, C. et al. (1997), ApJ, 479, 119](http://adsabs.harvard.edu/abs/1997ApJ...479..119A)<br>
[Wozniak, P & Paczyński,B. (1997), ApJ, 487, 55](http://adsabs.harvard.edu/abs/1997ApJ...487...55W)<br>
[Han, C. (1999), MNRAS, 309, 373](http://adsabs.harvard.edu/abs/1999MNRAS.309..404H)<br>
[Street et al. (2013) ApJ, 763, id.67](https://ui.adsabs.harvard.edu/abs/2013ApJ...763...67S/abstract)