---
title: "Blended light degeneracy"
permalink: /theory/degeneracies/blended-light-degeneracy/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
Microlensing events are most frequently detected in crowded star fields, where 
there are substantial populations of sources and foreground lensing objects.  
Unfortunately, the density of the stars can result in blending, with the Point 
Spread Functions (PSFs) of stars overlap.  This is discussed in detail in [blending](/theory/blending/). 

Blended light from nearby stars can lead to degeneracies in two cases, described 
by [Woźniac and Paczyński (1997)](https://iopscience.iop.org/article/10.1086/304607).  

## Large impact parameters
Recall that $$A_{\rm tot} = \frac{u^{2}+2}{u\sqrt{u^{2} + 4}}$$, where the impact
parameter u is given by 
$$u^{2}(t) = u_{0}^{2} + \left ( \frac{t - t{0}}{t_{0}} \right )^{2}$$, reaching 
a minimum of $$u_{0}$$ at $$t_{0}$$.  For a source star of unlensed flux, 
$$F_{s,0}$$, the magnified flux as a function of time is given by 
$$F_{s}(t) = F_{s,0} A(t)$$.  Here, the baseline flux (before and after the event) 
<i>measured</i> from the blended stars, $$F_{0}$$, is a combination of flux 
from the source and other stars. 

Where $$u_{0}>>1$$, the expression for magnification becomes
$$A \approx = 1 + \frac{2}{u^{4}} = 1 + \frac{2}{[u_{0}^{2} + (t/t_{E})^{2}]^{2}}$$, 
where $$t_{0}$$ = 0. 

Using these equations, we can derive an expression for the ratio between the source 
and total flux in the limit where $$u_{0} << 1$$. 

$$\frac{F(t)}{F_{0}} = (1 - f_{s}) + f_{s} \left( 1 + \frac{2}{(u_{0}^{2} + (t/t_{E})^{2})^{2}} \right) = 1 + \frac{2 f_{s}}{(u_{0}^{2} + (t/t_{E})^{2})^{2}}$$,
 where $$f_{s}$$ is the fraction of the measured light coming from the source. 

Woźniac & Paczyński demonstrated that it is possible to substitute 

$$f_{s}^{\prime} = f_{s}C^{4}, u_{0}^{\prime} = u_{0} C, t_{E}^{\prime} = t_{E} C^{-1}$$ 
where C is an arbitrary positive constant into the equation above and still obtain the same expression for the flux ratio. 

This means that there is a degeneracy between blended flux, impact parameter and the Einstein crossing 
time.  The additional flux makes the event brighter at baseline 
than the true source alone, and effectively means that the event can appear to 
have a longer t<sub>E</sub> and lower impact parameter than it actually does. 

<figure>
  <img src="{{ '/assets/images/blending_degen_large_u0.png' | relative_url }}" alt="Comparison of degenerate blended and non-blended lightcurves" style="width:100%;">
  <figcaption>
    Comparison of degenerate blended and non-blended lightcurves [R.A.Street]</figcaption>
</figure>

An important aspect to note here is that although formally this degeneracy 
affects events with impact parameters greater than 1.0, in practise it is 
significant at smaller impact parameters as in the plotted example.  