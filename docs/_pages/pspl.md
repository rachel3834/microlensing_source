---
title: "Point Source, Point Lens"
permalink: /theory/pspl/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
The simplest case of microlensing consists of a single star as the source and a single star (or planet) as the lens, 
where both objects are treated as point masses.  Of course, the stars don't remain in alignment for long, so 
microlenses are transient events, which offer a fleeting glimpse of an unseen intervening system, never to be repeated.</p>

## Point Source, Point Lens
Figure 1 shows a lensing object passing close to the observer's line of sight to a background source star. As Einstein described
in General Relativity (G.R.), the light rays from the source passing close to the lens are deflected by its gravity.

The symbols have the following definitions:<br
D<sub>L</sub> = distance of the lens from the observer <br>
D<sub>S</sub> = distance of the source from the observer <br>
D<sub>LS</sub> = distance of the lens from the source<br>
M<sub>L</sub> = mass of the lens<br>
&alpha; = angular separation of the lens from the observer-source line of sight<br>
&theta;<sub>1,2</sub> = angular separation of images of the source from the center of the lens <br>
&epsilon;<sub>1,2</sub> = deflection of a light ray passing at radius r from the lens.<br>

<figure>
  <img src="{{ '/assets/images/lensing_geometry_side_view.png' | relative_url }}" alt="The geometry of a microlensing event." width="200">
  <figcaption>The geometry of a microlensing event. The red lines indicate the paths taken by light rays from the source. [R.A.Street]</figcaption>
</figure>

The closer the light rays get to the lens, the more they are deflected, according to Einstein's equation:
$$\epsilon = \frac{4GM_{L}}{rc^{2}}$$ [1]

Like any lens, the foreground object creates images of the light source. Consider a light ray leaving the source. It's path is
deflected and it reaches the observer, who sees a corresponding image of the source, at an angular separation from the source's
true position on the sky.

We will assume that the distances involved are sufficiently large that standard geometric small angle approximations are valid.

From Fig. 1, we observe the following relationships:<br>
* The angular displacement of the first image from the center of the lens, &theta;, is: 
$$\theta_{1} = \alpha + \beta$$ [2]
* As a triangle is formed between the observer, source and point B, the angles:
$$\beta + \beta^{\prime} + b^{\prime} = 180^{\circ}$$ [3]
* Since the line of sight between the observer and S1 image must be straight:
$$b^{\prime} + \epsilon_{1} = 180^{\circ}$$
Therefore: $$\beta + \beta^{\prime} + 180 - \epsilon_{1} = 180^{\circ},$$
So:<br>
$$\epsilon_{1} = \beta + \beta^{\prime}$$ [4]
* Angles &beta; and &beta;' scale with the ratio of the distances observer-lens and lens-source:<br>
$$\beta^{\prime} = \beta \left( \frac{D_{L}}{D_{LS}} \right)$$ [5]

* Combining these observations, we can derive an expression for the angular displacement of the image in terms of the 
G.R. deflection of light:
$$\epsilon_{1} = \beta + \beta \left( \frac{D_{L}}{D_{LS}} \right) = \beta \left( 1 + \frac{D_{L}}{D_{LS}} \right)$$

For convenience, we define $$\mu = 1 + D_{L}/D_{LS},$$ giving:
$$\theta_{1} = \alpha + \frac{\epsilon_{1}}{\mu}$$ [6]

Now, from G.R., $$\epsilon_{1} = \frac{4GM_{L}}{rc^{2}}.$$

$$\sin(\theta_{1}) = \frac{r}{D_{L}},$$ but for small angles we can say that $$r \sim D_{L}\theta_{1}.$$ So:
$$\epsilon_{1} = \frac{4GM_{L}}{\theta_{1}D_{L}c^{2}}$$ [7]

## The Lens Equation
By substituting [7] into [6], we derive the gravitational lens equation:

<table width="75%">
    <tr><td>$$\theta_{1} = \alpha + \frac{4GM_{L}}{\mu\theta_{1}D_{L}c^{2}}$$</td><td></td></tr>
    <tr><td>$$\mu\theta_{1}^{2}D_{L}c^{2} = \alpha\mu\theta_{1}D_{L}c^{2} + 4GM_{L}$$</td><td></td></tr>
    <tr><td>$$\theta_{1}^{2} - \alpha\theta_{1} - \frac{4GM_{L}}{\mu D_{L}c^{2}} = 0$$</td><td>[8]</td></tr>
</table>

Notice how all of the constants are clustered in the last term on the left of eqn. [8]. 
This term depends on fundamental constants plus the characteristics of the lensing system - M<sub>L</sub>, D<sub>L</sub>. 
So this term describes a  characteristic angular radius of the system: it is the angular Einstein radius,
&theta;<sub>0</sub>:

$$\theta_{0} = \sqrt{ \frac{4GM_{L}}{\mu D_{L} c^{2}}}.$$ [9]

The lens equation can then be written as a quadratic function:

$$\theta_{1}^{2} - \alpha\theta_{1} - \theta_{0}^{2} = 0$$ [10]

...and quadratic functions can be solved to find two roots using the standard mathematical formula:
$$x = \frac{-B\pm\sqrt{B^{2}-4AC}}{2A}$$,
where A, B, C are the coefficients of the quadratic equation, in this case A=1, B=-&alpha;, C=-&theta;<sub>0</sub><sup>2</sup>.
So we solve the lens equation:
$$\theta_{1} = \frac{+\alpha+\sqrt{\alpha^{2}+4\theta_{0}^{2}}}{2} = \frac{1}{2}\alpha + \left[ \left( \frac{1}{2}\alpha \right)^{2} + \theta_{0}^{2}\right]^{\frac{1}{2}}$$ [11]

and similarly:
$$\theta_{2} = -\frac{1}{2}\alpha + \left[ \left( \frac{1}{2}\alpha \right)^{2} + \theta_{0}^{2} \right]^{\frac{1}{2}}$$ [11]

From this, we understand that the observer always see two images of the source created during a lensing event by a single,
point lensing body and can predict their positions. The only exception to this occurs if the alignment of the lens along the
line of sight to the source is perfect = that is, &alpha; = 0. From Eqn. 10, we see that both images then have the same angular
separation. In this special case, the image of the source that the observer sees is a perfect ring at the Einstein radius. In all
other cases, the images form arcs.

It's important to remember that there is no change in the surface brightness of the source during a lensing event - the light is
simply redistributed, and always conserved. As a result, the observer receives more flux from the source, which appears to brighten
during the lensing event, even while the source itself remains at constant brightness. As the lens moves away from the observer's
line of sight to the source, the latter appears to gradually return to its normal brightness.

We now shift our perspective, and consider the same lensing event from the observer's point of view, shown in Fig. 2. In this
lens-centric geometry, we define:
r<sub>0</sub> = separation of the source from the lens<br>
r<sub>1,2</sub> = separation of the images of the source from the lens<br>
R<sub>E</sub> = Einstein radius.<br>

<figure>
  <img src="{{ '/assets/images/lensed_image_geometry.png' | relative_url }}" alt="The geometry of a microlensing event, seen from the observer's perspective." width="200">
  <figcaption>The geometry of a microlensing event, seen from the observer's perspective. Here we look down the line of sight, with a coordinate system centered on the lens for convenience. Notice that the images of the source always form with one inside and one outside the Einstein radius of the lens. [R.A.Street]</figcaption>
</figure>

We can re-write the lens equation and its solutions in terms of radial distances from the lens projected on sky:
$$r^{2} - r_{0}r - R_{E}^{2} = 0,$$ [12]
where, to use the commonly-used notation of Paczyński (1986) and others,
$$R_{E}^{2} = \frac{4GM_{L}D}{c^{2}}$$, $$D = \frac{D_{L}D_{LS}}{D_{S}}.$$ [13]

The solutions of this, i.e. the projected locations of the images, are then:
$$r_{1,2} = \frac{r_{0}\pm(r_{0}^{2}+4R_{E}^{2})^{\frac{1}{2}}}{2}.$$ [14]

## References
[Liebes, S. (1964), Physical Review, 133, B835](http://adsabs.harvard.edu/abs/1964PhRv..133..835L)<br>
[Paczyński, B. (1986), ApJ, 301, 503](http://adsabs.harvard.edu/abs/1986ApJ...301..503P)<br>
[Wambsganss, J. (1998), Living Reviews in Relativity, 1, 12](http://adsabs.harvard.edu/abs/1998LRR.....1...12W)