---
title: "Jerk parallax degeneracy"
permalink: /theory/degeneracies/jerk-parallax-degeneracy/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
Microlensing events are highly sensitive to the alignment of the lens and source - and the 
observer.  As we discussed in [parallax](/theory/parallax/), the movement of the Earth 
around the Sun during an event is sometimes enough to measurably change the observed impact 
parameter.  In cases were annual parallax is significant, typically models use the approach of 
[Smith, Mao & Paczyński (2003)](https://ui.adsabs.harvard.edu/abs/2003MNRAS.339..925S/abstract) and
include the acceleration of the Earth in it's orbit.  

Very occasionally the acceleration alone is insufficient, as it was for an early 
event detected in the Magellanic Cloud, MACHO-LMC-5 ([Alcock et al.(2001)](https://www.nature.com/articles/414617a)).  
[Gould (2004)](https://ui.adsabs.harvard.edu/abs/2004ApJ...606..319G/abstract) concluded that 
the jerk (the rate of change in the acceleration) must also be taken into account.  Here 
we discuss his arguments.  The same phenomenon has also been detected for events in the 
Galactic bulge, such as MOA 2003-BLG-37 [Park et al.(2004)](https://ui.adsabs.harvard.edu/abs/2004ApJ...609..166P/abstract).

## Geocentric coordinate system
Firstly, let's establish a frame of reference.  Since we generally observe microlensing 
events from Earth, it is easiest to represent those data using a geocentric coordinate system. 

<figure>
  <img src="{{ '/assets/images/sun_earth_geometry.png' | relative_url }}" alt="Illustration of the Earth in orbit about the Sun" style="width:100%;">
  <figcaption>
    Illustration of the Sun-Earth coordinate system [R.A.Street]</figcaption>
</figure>

$$\mathbf{s}(t)$$ represents the Sun-to-Earth vector in units of AU (i.e. in the heliocentric frame). 
The derivative of this can be taken at time $$t_{p}$$, $$\mathbf{v_{p}} = \left. \frac{d\mathbf{s}}{dt} \right|_{t_{p}}$$, 
where $$t_{p}$$ is typically chosen to be close to $$t_{0}$$. 

To convert to the geometric frame, we need to transform the Sun's positional vector, 
giving it an offset of $$\mathbf{\Delta s}(t) = \mathbf{s}(t) - (t - t_{p})\mathbf{v_{p}} - \mathbf{s}(t_{p})$$.  
If we define unit vectors $$\mathbf{\hat{n}}$$ and $$\mathbf{\hat{e}}$$ pointing north 
and east, then we can write the projected position of the Sun in a right-handed coordinate system as:

$$(s_{n}, s_{e}) = (\mathbf{\Delta s} \cdot \mathbf{\hat{n}}, \mathbf{\Delta s} \cdot \mathbf{\hat{e}}).$$

We can now define the coordinates of the lens relative to the source $$(\tau, \beta)$$ in units of the 
angular Einstein radius:

$$\tau(t) = \frac{t - t_{0}}{t_{E}} + \delta \tau, \beta(t) = u_{0} + \delta\beta,$$

where the change $$(\delta \tau, \delta \beta)$$ can be described in terms of $$\mathbf{\Delta s}$$:

$$
\begin{aligned}
(\delta \tau, \delta \beta) = \pi_{E}\mathbf{\Delta s} &= (\mathbf{pi_{E}} \cdot \mathbf{\Delta s}, \mathbf{pi_{E}} \times \mathbf{\Delta s}) \\ 
&= [s_{n}(t)\pi_{E,N} + s_{e}(t)\pi_{E,E}, -s_{n}(t)\pi_{E,E} + s_{e}(t)\pi_{E,N}].
\end{aligned}
$$

$$(\tau,\beta)$$ is also defined to be right-handed, such that if the lens passes to the right 
of the source as seen from Earth for positive values of $$u_{0}$$.  

These equations define the “vector microlens parallax” $$\mathbf{\pi_{E}} = (\pi_{E,N}, \pi_{E,E})$$,
The magnitude, $$\pi_{E} = |\mathbf{\pi_{E}}|$$ is related to the projected size of the 
Einstein ring, $$\tilde{r_{E}}$$, by $$\tilde{r_{E}} = AU/\pi_{E}$$.  

## Acceleration and jerk of the Sun relative to the Earth
Gould (2004)'s initial modeling of MACHO-LMC-5 factored in the affects of annual parallax 
following the method of [Alcock et al.(2001)](https://www.nature.com/articles/414617a), who 
considered the velocity and acceleration terms in Earth's orbit.  

<figure>
  <img src="{{ '/assets/images/gould2004_fig3.png' | relative_url }}" alt="Likelihood contours in the annual parallax plane for MACHO-LMC-5" style="width:100%;">
  <figcaption>
    Likelihood contours in the annual parallax plane for MACHO-LMC-5 [Gould (2004), Fig.3].  Contours are shown for &Delta; &chi;<sup>2</sup>2=1,4,9,16,25,36 & 49 relative to the minimum &chi;<sup>2</sup>.  
    Old and new annotations indicate solutions identified by Alcock et al.(2001) and Gould (2004). 
</figcaption>
</figure>

As illustrated in the plot above, Gould (2004) recovered Alcock's solution but found a 
second solution offset in the $$\pi_{E,\perp}$$ direction, perpendicular to the Earth's 
acceleration vector at the event peak.  Residual deviations remained in the lightcurve, 
spuring Gould to consider including the term for the second derivative of velocity - 
jerk - as well.  

The vector position of the lens relative to the source in the Einstein ring can be described 
as:

$$\mathbf{u} = \mathbf{u_{0}} + \mathbf{\omega} t + \pi_{E}\left ( \frac{1}{2}\mathbf{\alpha} t^{2} + \frac{1}{6}\mathbf{j}t^{3} + ... \right ),$$

where $$\mathbf{u_{0}}$$ is the vector impact parameter, $$\mathbf{\omega} = t_{E}^{-1}$$ is the vector 
inverse timescale, and $$\mathbf{\alpha}$$ and $$\mathbf{j}$$ are the apparent acceleration and 
jerk of the Sun relative to the Earth both divided by 1 AU.  $$\mathbf{\omega}, \mathbf{\alpha}$$ 
and $$\mathbf{j}$$ are all two-dimensional vectors evaluated at t = 0.  
$$\mathbf{u_{0}} \cdot \mathbf{\omega} = 0$$ is required, based on the assumption that $$t_{0}$$
can be determined from the lightcurve.  

This expression can be written as a series summation with the following co-efficients:

$$u^{2} = \sum_{i=0}^{\infty} C_{i} t^{i},$$

$$C_{0} = u_{0}^{2}, C_{1} = 0, C_{2} = -\alpha u_{0} \pi_{E, \perp} + t_{E}^{-2},$$

$$C_{3} = \alpha \frac{\pi_{E,\parallel}}{t_{E}} + \frac{1}{4}\alpha^{2}t_{E}u_{0} \mathbf{\pi_{E}} \times \mathbf{\pi_{j}},$$

$$C_{4} = \frac{\alpha^{2}}{4}(\pi_{E}^{2} + \mathbf{\pi_{j}} \cdot \mathbf{\pi_{E}}) + \frac{1}{12}\frac{\Omega^{2}_{\oplus}}{\alpha} u_{0}\pi_{E, \perp},$$

where

$$\mathbf{\pi_{j}} = \frac{4}{3} \frac{\mathbf{j}}{\alpha^{2}t_{E}}, $$

represents the jerk parallax and the $$||$$ and $$\perp$$ notation refers to 
components that are parallel and perpendicular to the acceleration.  The Earth's 
orbit is approximated to be a circle, such that the derivative of the jerk is $$-\Omega_{\oplus}^{2}\mathbf{\alpha}$$ 
where $$\Omega_{\oplus} = 2\pi yr^{-1}$$.  

This formulation has the practical advantage that the constants $$C_{0-4}$$ can be 
determined empirically if $$u_{0}, t_{E}, \mathbf{\pi_{E}}$$ can be measured from 
an event's lightcurve.  

In the limit where $$u_{0} \to 0$$ the expressions for co-efficients $$C_{3,4}$$ become:

$$C_{3} = \alpha \frac{\pi_{E,||}}{t_{E}}, C_{4} = \frac{\alpha^{2}}{4}(\pi_{E}^{2} + \mathbf{\pi_{E}} \cdot \mathbf{\pi_{j}}).$$

But this case exhibits the degeneracy such that

$$\pi_{E,||}^{\prime} = \pi_{E,||}, \pi_{E,\perp}^{\prime} = -(\pi_{E,\perp} + \pi_{j,\perp}), t_{E}^{\prime} = t_{E}, $$

These expressions have one exception in the special case where 
$$\pi_{E,\perp} = -\pi_{j,\perp}/2$$ and $$\mathbf{\pi_{E}^{\prime}} = \mathbf{\pi_{E}}$$, 
and the degeneracy is broken. 


## References
[Alcock, C., et al. 2001, Nature, 414, 617](https://www.nature.com/articles/414617a)
[Gould (2004), ApJ, 606, 319](https://ui.adsabs.harvard.edu/abs/2004ApJ...606..319G/abstract)<br>
[Park et al.(2004) ApJ, 609, 166](https://ui.adsabs.harvard.edu/abs/2004ApJ...609..166P/abstract)<br>
[Smith, Mao, Paczyński (2003), MNRAS, 339, 925](https://ui.adsabs.harvard.edu/abs/2003MNRAS.339..925S/abstract)