---
title: "Estimating Parameters"
permalink: /theory/estimating-parameters/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
The light curve of a microlensing event encodes a great deal of information.  Indeed, 
many of the most important parameters can be estimated directly from timeseries 
photometry, and it is helpful to know how to build physical intuition about the events. 

## Parameterization of a Point Lens Lightcurve

<p>A point lens microlensing event is parameterized by three variables: </p>

<ul style="list-style-type:none">
  <li><i>u</i><sub>0</sub> = the impact parameter between the source and the lens (i.e. minimum separation) </li>
  <li><i>t</i><sub>0</sub> = the time of closest approach between the source and lens (i.e. <i>t</i> at <i>u</i> = <i>u</i><sub>0</sub>)</li>
  <li><i>t</i><sub>E</sub> = the Einstein crossing time = the time for the source to travel 1 Einstein radius </li>
</ul>

<figure>
  <img src="{{ '/assets/images/geom_Aofu.png' | relative_url }}" alt="The geometry of a microlensing event, seen from the observer's perspective." width="200">
  <figcaption>Geometry of a point source, point lens event [Y.C. Yee]</figcaption>
</figure>

The magnification of the source is given by the equation:

$$A(u) = \frac{u^2 + 2}{u (u2 + 4 )^{1/2}}$$

where $$u = ( u_0^2 + \tau^2)^{1/2}$$ and $$\tau = (t - t_0)/t_{E}$$.  

t<sub>0</sub> is easily estimated from the time of the peak of a point-source, point-lens lightcurve, 

<figure>
  <img src="{{ '/assets/images/geom_u0t0.png' | relative_url }}" alt="Estimating t0 and u0 for a point source, point lens event." width="200">
  <figcaption>Estimating t0 and u0 for a point source, point lens event [Y.C. Yee]</figcaption>
</figure>

Next, we can measure the width of the peak in time at half of it's maximum magnification
to estimate the t<sub>FWHM</sub> of the lightcurve (FWHM = Full Width Half Maximum).  The 
Einstein crossing time, t<sub>E</sub>
can be calculated using the measured t<sub>FWHM</sub> and the above
equations. In the limit where <i>u</i><sub>0</sub> << 1, t<sub>E</sub>
~ (1/2)t<sub>FWHM</sub>/<i>u</i><sub>0</sub>.

<figure>
  <img src="{{ '/assets/images/geom_FWHM.png' | relative_url }}" alt="Estimating t0 and u0 for a point source, point lens event." width="200">
  <figcaption>Estimating t0 and u0 for a point source, point lens event [Y.C. Yee]</figcaption>
</figure>

## Extracting Planet Parameters
[Gaudi & Gould (1997)](http://adsabs.harvard.edu/abs/1997ApJ...486...85G) showed that the parameters of a planet (s and q) can be 
approximated analytically based on light curve observables.

Here we use their techniques to estimate the parameters of a planetary event. 

### Finding the Location of the Planet

First, determine the parameters of the underlying stellar event
( <i>t</i><sub>0</sub>, <i>u</i><sub>0</sub>, <i>t</i><sub>E</sub>)
following the method above. Then, measure the time of the planetary perturbation 
<i>t</i><sub>p</sub>:</p>

<figure>
  <img src="{{ '/assets/images/planet_lc_annotated.png' | relative_url }}" alt="Estimating the time of planetary perturbation" width="200">
  <figcaption>Estimating tp, the time of planetary perturbation [Y.C. Yee]</figcaption>
</figure>

Combined with the point lens parameters, you can calculate $$\tau$$ and therefore, <i>u</i> at that time. 
This gives the source position relative to the lens. Since a planet must perturb 
one of the images to be detected, to first order, this means the planet must be at 
the location of one of the images:

<figure>
  <img src="{{ '/assets/images/images_plus.png' | relative_url }}" alt="Location of major and minor images during a lensing event" style="max-width:600px; width:80%;">
  <figcaption>Location of major and minor images during a lensing event [Y.C. Yee]</figcaption>
</figure>

The position of the images is given by: y<sub>&#177</sub> = &#177
(&frac12;) (&#8730(u<sup>2</sup> + 4) &#177 u), so the planet
location, <i>s</i> must be either <i>y</i><sub>+</sub>
or <i>y</i><sub>-</sub>.

If the planet perturbs the minor image, it will tend to destroy
that image, leading to a decrease in magnification. On the other
hand, a planet will always further magnify a major image:

<figure>
  <img src="{{ '/assets/images/planet_minor.png' | relative_url }}" alt="Lightcurve with planet close to the minor image" style="max-width:600px; width:80%;">
  <img src="{{ '/assets/images/planet_major.png' | relative_url }}" alt="Lightcurve with planet close to the major image" style="max-width:600px; width:80%;">
  <figcaption>Lightcurve with planet close to the minor image (left) and major image (right) [Y.C. Yee]</figcaption>
</figure>

Therefore, the form of the perturbation will show which solution
is correct.

## Finding the Mass Ratio of the Planet

The size of the Einstein ring is proportional to the square root of the mass:
Einstein Ring = $$>\theta_{E} \propto M^{1/2}$$.  Therefore, the ratio of the duration 
of the planetary perturbation to the duration of the event should be proportional to 
the square root of the mass ratio. 

Equivalently, mass ratio $$=  q = \frac{m_p}{M_{star}} = \frac{t_{E,p}^{2}}{t_{E,star}^{2}}$$. 

## References
[Gaudi & Gould (1997)](http://adsabs.harvard.edu/abs/1997ApJ...486...85G)