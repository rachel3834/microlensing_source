---
title: "Optical Depth"
permalink: /theory/optical-depth/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
So far we've concluded that although we cannot resolve the individual images created during microlensing, we might detect these
events from the amplification of the source. But the alignment required between observer, lens and source for an event is extremely
tight, so what are the odds of this ever happening?

## "Threshold" Amplification
To look at the probability of an event occuring, we need a clear criterion for deciding that an event is underway. From the
amplification equation:

<table width="75%"><tr><td>$$A = \frac{u^{2}+2}{u(u^{2}+4)^{1/2}}$$</td><td>[24]</td></tr></table>

where u &equiv; &alpha;/&theta;<sub>0</sub> &equiv; r<sub>0</sub>/R<sub>0</sub>,

...we see that the amplification tends towards 1 at infinite angular separation. For the purposes of this discussion, we will
consider microlensing events from the magnification they reach when &alpha; = &theta;<sub>0</sub>, A<sub>0</sub> &sim; 1.34.

## Optical Depth to Microlensing
The optical depth is defined to be the probability that a given star, at a specific instant in time, has an amplification caused
by gravitational microlensing of A &#8827; 1.34. This is the fraction 
of a given solid angle of sky observed which is covered by the Einstein rings of all lensing objects within that area.

Picture the sky as an observer sees it: a surface enclosing a spherical volume around the observer's location. Let the area of
that spherical surface which the observer can view be represented by d&Omega;, and let's consider all lensing objects with distances
out to D<sub>L</sub>. The optical depth needs to sum over the area covered by the Einstein radii of all lenses out to this distance.

The total solid angle subtended by the Einstein rings of all events within a given volume is the area of a given lens's Einstein
ring with the number of lenses in the volume observed. Representing this as a fraction of the total area of sky included gives us
the optical depth of microlensing, &tau;:

<table width="75%"><tr><td>$$\tau = \frac{1}{d\Omega} \int d V n(D_{d})\pi \theta_{0}^{2},$$</td><td>[25]</td></tr></table>

where n(D<sub>L</sub>) is the number density of lenses. From spherical trigonometry, the volume, dV , enclosed by the observer's
field of view out to D<sub>L</sub> is given by:

<table width="75%"><tr><td>$$dV = d\Omega D_{L}^{2} dD_{L}$$</td><td>[26]</td></tr></table>

Substituting Eqn. 9 for &theta;<sub>0</sub>, and allowing &rho; to represent the average mass density due to lenses,
&rho; = M<sub>L</sub>n(Dd)/dV, we get:

<table width="75%"><tr><td>$$\tau = \int_{0}^{D_{S}} \frac{4\pi G \rho D_{L} D_{LS}}{D_{S}c^{2}} d D_{L}$$</td><td>[27]</td></tr></table>

For mathematical simplicity, let's substitute x = D<sub>L</sub>/D<sub>S</sub>:

<table width="75%"><tr><td>$$\tau = \frac{4\pi G}{c^{2}}D_{S}^{2} \int_{0}^{D_{S}} \rho(x)x(1-x)dx$$</td><td>[27]</td></tr></table>

In the general case, we would need to evaluate this integral with a realistic model for the density distribution of matter. However, if we assume that the
density distribution is constant, we can derive an exact expression for &tau;:

<table width="75%"><tr><td>$$\tau = \frac{2\pi}{3} \frac{G \rho}{c^{2}} D_{S}^{2}$$</td><td>[28]</td></tr></table>

Note how this is quantity tells us about the density of lensing objects; that is, it tells us something about the population of
unseen bodies. However, it depends on the <i>total mass</i> over total volume - rather than the masses of individual lenses.

## Measurements of the Microlensing Optical Depth

A couple of microlensing surveys have measured the lensing optical depth towards the Galactic Bulge, notably OGLE (see
Paczyński, B. et al. 1994) and MACHO (Alcock, C. et al 1997).
Read these papers to learn how. Compare this with the discussions in Paczyński, B. (1986) and Paczyński, B.
(1991). Using the measured &tau;, and the size of the OGLE-II catalog (available online), and assuming for the sake
of argument that all stars within the catalog are observed continuously & perfectly, estimate the number of microlensing events we
could expect to see over the course of the Bulge observing season (April-October).

## References
[Alcock, C. et al. (1997), ApJ, 479, 119](http://adsabs.harvard.edu/abs/1997ApJ...479..119A)<br>
[Paczyński, B. et al. (1994), ApJ, 435, L113](http://adsabs.harvard.edu/abs/1994ApJ...435L.113P)<br>
[Paczyński, B. (1986), ApJ, 304, 1](http://adsabs.harvard.edu/abs/1986ApJ...304....1P)<br>
[Paczyński, B. (1991), ApJ, 371, L63](http://adsabs.harvard.edu/abs/1991ApJ...371L..63P)
