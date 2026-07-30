---
title: "Finite Source Effects"
permalink: /theory/finite-source-effects/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
Stars lie at such great distances from Earth that it is normally safe to treat them as 
if they were just points of light.  Of course in reality they have a finite diameter.  
In some cases of microlensing, this diameter has a measureable affect on the 
light curve, known as "finite source effects".

To understand why this is the case, let's take a closer look at how light 
from the source star is deflected by the lens. 

## Lens to source plane mapping
<figure>
  <img src="{{ '/assets/images/lens_source_plane_mapping.png' | relative_url }}" alt="Illustration of the lens and source planets in a microlensing event" width="200">
  <figcaption>Illustration of the lens and source planets in a microlensing 
event.  &theta;<sub>1,2</sub> are the angular offsets of source images, 
&theta;<sub>E</sub> is the angular Einstein radius and &theta; is the angular separation between 
lens and source.  [R.A.Street]</figcaption>
</figure>

The lensing equation shows us that for each point in the plane of the lens, there 
is an equivalent point in the source plane; in other words, we can map the 
coordinate system of the lens plane (x,y, centered on the lens) to the source plane
 coordinates (&xi;, &eta;).

## Radial profile of a star
When we observe a star, we do not receive a uniform amount of light from all points 
across it's disk.  The light coming from the limb of the star has to pass through 
more of the stars atmosphere than that coming from the center.  As a result, stars 
exhibit <i>limb darkening</i> as shown in the figure below.  

<table>
<tr>
<td>
<figure>
  <img src="{{ '/assets/images/limb_darkening_gradient.png' | relative_url }}" alt="Radial profile of a star" style="width:300px;">
</figure>
</td>
<td>
The radial profile of a star illustrating the annuli across it's surface. [R.A.Street]
</td>
</tr>
</table>
It is this non-uniform brightness profile that causes the finite source effects 
in microlensing light curves.  We need to adapt our equations to calculate the 
magnification to take this into account.  

As a reminder the parameters in the lensing equations representing the source 
star are:

R<sub>S</sub>: source star physical radius<br>
&theta;<sub>*</sub>: source star angular radius<br>
&rho;:  &theta;<sub>*</sub> normalized by the angular Einstein radius &theta;<sub>E</sub>. 

## The parameterized lens equation
To incorporate finite source effects into the lens equation, we first need 
to parameterize it, which is most easily done using complex notation.  
So we introduce the following notation to represent (x,y) and (&xi;, &eta;) coordinates:

$$z = x + iy$$

$$\zeta = \xi + i \eta, $$

where z and &zeta; are normalized to the Einstein radius in the lens, source planes respectively.

The lens equation for a single lens then becomes:

$$\zeta - \frac{D_{S}}{D_{L}}z - D_{LS}\alpha(z,\bar{z}) = 0,$$

where &alpha; is the complex deflection angle 

$$\alpha(z, \bar{z}̄) = \alpha_{x}(x, y) + i\alpha_{y}(x, y)$$

and $$\bar{z}̄$$ is the complex conjugate of z.

The solutions of this form of the lens equation can then be written as:

$$z_{1,2} = \frac{\xi}{2} \left( 1 \pm \sqrt{1 + \frac{4}{\zeta \xi}} \right)$$

## Lens equation for sources of finite extent
Using our parameterized notation, we can describe a circular star of radius r as follows:

$$\zeta(\phi) = \zeta_{0} + re^{i\phi},$$

where $$\phi = \theta - 2\pi$$ and &zeta;<sub>0</sub> is the (parameterized) 
impact parameter.  Substituting this into the parameterized lens equation, we 
can derive an expression for the image positions:

$$z_{1,2} = \frac{\zeta_{0} + re^{i\phi}}{2} \left[ 1 \pm \sqrt{1 + \frac{4}{\zeta_{0}^{2} + 2r\zeta_{0}\cos{\phi} + r^{2}}} \right]$$.

## Calculating magnification including finite source effects
We can now use our parameterized equations to calculate the magnification during 
a microlensing event.  As for a point source, the magnification A<sub>tot</sub> 
is equal to the ratio of the combined image area of the lensed versus the unlensed source. 
In complex notation this can be expressed as the integral over the area of 
the disk of the star:

$$A_{1,2} = \frac{1}{2\pi r^{2}} \int_{0}^{2\pi} y(\phi) \frac{dx(\phi)}{d\phi}$$,

where

$$x(\phi) = \frac{\zeta_{0} + r\cos{\phi}}{2} f_{1,2}(\phi)$$,

$$y(\phi) = \frac{r\sin{\phi}}{2} f_{1,2}(\phi)$$,

and

$$f_{1,2}(\phi) = 1 \pm \sqrt{1 + \frac{4}{\zeta_{0}^{2} + r^{2} + 2\zeta_{0} r \cos{\phi}}}$$.

## Limb darkening
By expressing the magnification in terms of the radial extent of the source star, 
we have paved the way to factor in the non-uniformity of the star's flux 
as a result of limb darkening.  

There are a number of expressions for describing the intensity of the star's light 
as a function of radius, r, $$I_{\lambda}(r)$$.  They are normally given in 
ratio to the intensity at the center of the star, $$I_{\lambda}(0)$$.  

The expression most commonly used in microlensing was derived by Mao & Witt (1998):

$$\frac{I_{\lambda}(r)}{I_{\lambda}(0)} = 1 - u_{\lambda,1} - u_{\lambda,2} + u_{\lambda,1}\sqrt{1 - \frac{R_{S}^{2}}{r^{2}}} + u_{\lambda,2} \left( 1 - \frac{R_{S}^{2}}{r^{2}} \right)$$.

It's important to note that limb darkening is dependent on wavelength the coefficients, 
$$u_{\lambda,1,2}$$ varying with the spectral type of the star.  The  
coefficients are published (e.g. by [Claret et al (2011)](http://adsabs.harvard.edu/abs/2011A%26A...529A..75C)) as tables that can 
be [found on Vizier](https://vizier.cds.unistra.fr/viz-bin/VizieR?-source=J/A+A/529/A75).

## Observable impact of finite source effects
Finite source effects are only observed when the impact parameter is so small 
that it is comparable with the angular size of the source star, &theta;<sub>*</sub>.  
As a result it is only observed in a fraction of events, and while $$u > \theta_{*}$$ we 
can safely neglect finite source effects to make the calculations more efficient. 

When they are observed, finite source effects result in a 'rounding over' at 
the peak of the event when compared with a point source model.  This can effectively 
reduce the peak amplitude significantly.  This is reason why real-world events 
never reach the theoretical infinite magnification.  

<figure>
  <img src="{{ '/assets/images/sim_finite_source_lcs.png' | relative_url }}" alt="Illustration of the effect of finite source effects on a microlensing lightcurve" width="200">
  <figcaption>Illustration of the effect of finite source effects on a microlensing lightcurve.  [R.A.Street]</figcaption>
</figure>

## References
[Witt, H.J. (1990), A&A, 236, 311](http://adsabs.harvard.edu/abs/1990A%26A...236..311W)<br>
[Witt, H.J. & Mao, S. (1994), ApJ, 430, 505](http://adsabs.harvard.edu/abs/1994ApJ...430..505W)<br>
[Mao, S. & Witt, H.J. (1998), MNRAS, 300, 104](http://adsabs.harvard.edu/abs/1998MNRAS.300.1041M)<br>
[Claret, A & Bloemen, S. (2011), A&A, 529, 75](http://adsabs.harvard.edu/abs/2011A%26A...529A..75C)<br>

