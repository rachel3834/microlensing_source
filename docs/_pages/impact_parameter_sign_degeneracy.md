---
title: "Impact parameter sign degeneracy"
permalink: /theory/degeneracies/impact-parameter-sign-degeneracy/
layout: single
classes: wide
sidebar:
  nav: "main"
---

This degeneracy arises from symmetries in the caustic structure.  The caustic is defined in lens-centered 
coordinates, such that the impact parameter, u, can take positive and negative values. 

For the binary-lens case shown below, the lens-source relative trajectory means that 
the source intersects the caustic in two places where the magnification is 
identical, producing an identical lightcurve.  These points occur at u and -u.  

In point-source, point-lens models, the caustic is a point.  Since this is 
symmetrical from all directions, the models do not have an &alpha; parameter, but 
the same impact parameter degeneracy exists.  

<div class="container">
    <div class="row">
        <div class="col-md">
        <figure>
          <img src="{{ '/assets/images/caustic_plot_neg.png' | relative_url }}" alt="Caustic structure with source trajectory intersecting with negative impact parameter" style="width:300px;">
          <figcaption>
            Caustic structure with source trajectory intersecting with negative impact parameter [R.A.Street]</figcaption>
        </figure>
        </div>
        <div class="col-md">
        <figure>
          <img src="{{ '/assets/images/caustic_plot_pos.png' | relative_url }}" alt="Caustic structure with source trajectory intersecting with positive impact parameter." style="width:300px;">
          <figcaption>
            Caustic structure with source trajectory intersecting with positive impact parameter [R.A.Street]</figcaption>
        </figure>
        </div>
    </div>
    <div class="row">
        <div class="col-md">
        <figure>
          <img src="{{ '/assets/images/lc_plot_neg.png' | relative_url }}" alt="Lightcurve of source trajectory intersecting caustic with negative impact parameter" style="width:300px;">
          <figcaption>
        Lightcurve of source trajectory intersecting caustic with negative impact parameter [R.A.Street]</figcaption>
        </figure>
        </div>
        <div class="col-md">
        <figure>
          <img src="{{ '/assets/images/lc_plot_pos.png' | relative_url }}" alt="Lightcurve of Caustic source trajectory intersecting caustic with positive impact parameter" style="width:300px;">
          <figcaption>
         Lightcurve of source trajectory intersecting caustic with positive impact parameter [R.A.Street]</figcaption>
        </figure>
        </div>
    </div>
</div>

The same phenomena has been observered in events with a measureable annual parallax 
signature, such as [Dominik et al.(2018)](https://arxiv.org/abs/1808.03149).  
Parallax affects both single and multiple lens models by introducing a skew 
(or in extreme cases a sinusoidal curve) into the lightcurve on top of the 'static' 
microlensing signature, as illustrated below. 

<table>
<tr>
<td>
<figure>
  <img src="{{ '/assets/images/udegen_parallax_caustic_plot.png' | relative_url }}" alt="Caustic structures for relative source trajectories with and without parallax" style="width:500px;">
  <figcaption>
    Caustic structures (red) for relative source trajectories without (black) parallax, and with parallax with u<sub>0</sub>0 positive (magenta} and negative [R.A.Street]</figcaption>
</figure>
</td>
<td>
<figure>
  <img src="{{ '/assets/images/udegen_parallax_lc.png' | relative_url }}" alt="Lightcurves for binary models with and without parallax" style="width:500px;">
  <figcaption>
    Lightcurves for binary models without (black) parallax, and with parallax with u<sub>0</sub> positive (magenta} and negative (green) [R.A.Street]</figcaption>
</figure>
</td>
</tr>
</table>

The caustic for a given single or binary model remains the same shape; the effect 
of annual parallax is to introduce a curvature into the relative lens-source 
trajectory.  This is the result of the observer moving during the event.  
There is still a u<sub>0</sub> degeneracy if this curve trajectory intersects 
the caustic at the same angle &alpha; due to the symmetry of the caustic.  