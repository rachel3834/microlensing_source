---
title: "Finite source degeneracy"
permalink: /theory/degeneracies/finite-source-degeneracy/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

Finite source effects cause measurable distortions only around the peak of a microlensing lightcurve 
 if the angular radius of the source star is comparable with the impact parameter, u<sub>0</sub>. 

Degeneracies can arise if this region in the lightcurve is not well sampled.  A good example of this 
is event OGLE-2015-BLG-1482L analysed in [Chung et al.(2017)](https://ui.adsabs.harvard.edu/abs/2017ApJ...838..154C/abstract).  

<figure>
<img src="{{ '/assets/images/chung2017_fig1.jpg' | relative_url }}" alt="Lightcurve of OGLE-2015-BLG-1482L" style="width:500px;">
  <figcaption>
    Lightcurve of OGLE-2015-BLG-1482L showing alternative models with different angular source sizes. [Chung et al.(2017), Fig. 1]
  </figcaption>
</figure>

Observations were obtained from both ground-based observatories and the Spitzer Space Telescope for 
this event.  The ground-based lightcurves are well-sampled, but Spitzer obtained ~1 observation 
per day.  The Spitzer lightcurve was sufficient to measure the impact parameter, u, as seen from 
the spacecraft, as well as the source and blend fluxes, $$f_{s}, f_{b}$$.  But only one of the 
Spitzer datapoints was measurably impacted by finite source effects.  

For high magnification, point-source, point-lens events, we can state that the magnification 
$$A_{PSPL} \approx 1/u$$.  Since $$f_{s}, f_{b}$$ are measured, we can infer the (finite-source affected)
magnification, $$A_{obs}$$ at the time of the one datapoint near the peak using the measured flux F, 
of that point:

$$A_{obs} = \frac{F - f_{b}}{f_{s}}.$$

The ratio of $$A_{obs}$$ and $$A_{PSPL}$$ can therefore be measured directly from the lightcurve,
as shown by [Gould (1994)](https://ui.adsabs.harvard.edu/abs/1994ApJ...421L..71G/abstract):

$$B(z) \equiv \frac{A_{obs}}{A_{PSPL}} \approx A_{obs} u,$$

where $$z \equiv u/\rho$$.  Gould (1994) showed that B(z) reaches a maximum of $$1.34^{2}$$ when 
z~0.91.  Inverting a measurement of B(z), there is one solution of z for $$B_{obs} \lt 1$$, two 
solutions for $$1 \lt B_{obs} \lt 1.34$$ and no solutions for $$B_{obs} \gt 1.34$$. 

In the case of Spitzer's lightcurve for OGLE-2015-BLG-1482L, the one datapoint near the peak 
has $$A_{obs}$$=1.14 and u=0.06, giving B(z)=1.15, and hence two solutions for z.  

For binary events, the finite source degeneracy can result in ambiguous values of the binary 
separation, s, and mass radio, q.  A good example of this is the event KMT-2019-BLG-1339L, analysed 
by [Han et al.(2020)](https://arxiv.org/abs/2003.02375).  

<figure>
<img src="{{ '/assets/images/han2020_fig4.png' | relative_url }}" alt="Alternative caustic crossing models for KMT-2019-BLG-1339L" style="width:500px;">
  <figcaption>
    Alternative caustic crossing models for KMT-2019-BLG-1339L [Han et al.(2020), Fig. 4]
  </figcaption>
</figure>

Here, different binary lens separations and mass ratios combine with different source sizes 
to produce similar lightcurves.  These could be distinguished with higher resolution data, 
but this isn't always available. 

## Extreme Finite Source Events
When lensing is caused by an object of low mass, it is possible for the angular radius of the source 
star to exceed the angular Einstein radius of the lens.  This scenario was explored in depth by 
[Johnson et al.(2022)](https://ui.adsabs.harvard.edu/abs/2022ApJ...927...63J/abstract).  In these 
rare cases, the lens is analogous to a magnifying glass passing over the surface of the source star. 

Recalling the equation of magnification for a point source, 

$$A_{PS} = \frac{u^{2} + 2}{u\sqrt{u^{2} + 4}},$$

the flux measured during an event is described by:

$$F(t) = F_{s}A(t) + F_{b},$$

where $$F_{s}, F_{b}$$ refer to the source and blend flux. [Liebes (1964)]((https://ui.adsabs.harvard.edu/abs/1964PhRv..133..835L/abstract)) 
showed that the magnification of a finite source deviates from the expression above when $$u_{0} \le \rho/2$$, i.e. 
for high-magnification events. 
In these cases, the limb darkening of the source star must be taken into account.  It is common practise 
in microlensing to use a linear limb darkening law, with coefficient, &Gamma;, following a procedure 
introduced by [Yoo et al.(2004)](https://iopscience.iop.org/article/10.1086/381241).  

When $$\rho \gg 1$$, finite source effects are important for trajectories where the center of the lens 
passes within $$\theta_{*}$$ of the center of the source.  These events are modeled with 7 parameters
($$t_{0}$$, $$u_{0}$$, $$t_{E}$$, $$\rho$$, $$F_{s}$$, $$F_{b}$$, $$\Gamma$$), but only three quantities 
can be measured directly from the lightcurve: ($$t_{0}$$, $$\Delta F_{max}$$, $$t_{FWHM}$$).  

<figure>
<img src="{{ '/assets/images/johnson2022_fig1.png' | relative_url }}" alt="Lens plane geometry and lightcurves for extreme finite source events with a range of rho values" style="width:100%;">
  <figcaption>
    Lens plane geometry (left) and magnification curves (right) for extreme finite source events with a 
   range of rho values $$\rho$$ = (10, 12, ..., 24), i.e. decreasing angular Einstein radius.  The events 
   have the same angular source size, impact parameter and relative proper motion. [Johnson et al.(2022), Fig. 1]
  </figcaption>
</figure>

The figure above, from [Johnson et al.(2022)](https://ui.adsabs.harvard.edu/abs/2022ApJ...927...63J/abstract), illustrates 
the finite source effects produced when &rho; is varied across extreme 
values while all other parameters remain fixed.  The flux was normalized to the baseline and no 
blending was included.  This shows that $$\Delta F_{max}$$ increases as $$\rho$$ decreases (i.e. 
the angular Einstein radius of the lens decresses).  For larger values of $$\rho$$, the lightcurve 
flattens off at the top.  As a result, the duration of the event is no longer given by the source 
crossing time, $$t_{*}$$, but is better approximated by twice the source half-chord crossing time:

$$t_{c} = \frac{\theta_{*}}{\mu_{rel}}\sqrt{1 - \left ( \frac{u_{0}}{\rho} \right )^{2}  } = t_{*}\sqrt{1 - b_{0}^2} = \beta t_{*},$$

where $$\beta = \sqrt{1 - b_{0}^{2}}$$ and $$b_{0} = u_{0}/\rho$$ is the minimum source-lens angular separation 
in units of $$\theta_{*}$$ rather than the usual $$\theta_{E}$$.  This expression for the event 
duration is independent of $$\theta_{E}$$ and hence the mass of the lens.  

However, the morphology of the lightcurve also depends on the impact parameter, as demonstrated in the figure below. 

<figure>
<img src="{{ '/assets/images/johnson2022_fig2.png' | relative_url }}" alt="Lens plane geometry and lightcurves for extreme finite source events with a range of impact parameters" style="width:100%;">
  <figcaption>
    Lens plane geometry (left) and magnification curves (right) for extreme finite source events with a 
   range of impact parameter values, while keeping the Einstein radius (black circle) the same. [Johnson et al.(2022), Fig. 2]
  </figcaption>
</figure>

Here we see that the $$t_{FWHM}$$ decreases with increasing $$b_{0}$$.  At low impact parameters, 
the same boxy lightcurve shape is seen.  This has the following implications in extreme cases of finite source effects:

* the magnification during the event is effectively constant and depends only on $$\rho$$. As a result, 
the change in flux is contant and $$\Delta F \propto 2F_{s}/\rho^{2}$$;
* the timescale of the event is independent of $$\theta_{E}$$ and hence of lens mass;
* the magnification is independent of duration. 

The reason that the lighcurve profile has rounded corners rather than a square, top-hat profile 
is the finite size of the angular Einstein ring radius relative to the angular radius of the source. 
During the phases where the lens enters and leaves the disk of the source, the lightcurve is 
rounded over for a timescale, $$t_{ws} \equiv t_{E}/\beta$$.  This can be conveniently 
written as a fraction, $$f_{ws}$$, of the event duration, $$t_{c}$$:

$$f_{ws} \equiv \frac{t_{ws}}{t_{c}} = (\beta \rho)^{-1}.$$

The duration of these "wings" and "shoulders" increases with increasing impact parameter, but also 
with decreasing $$\rho$$.  

### Extreme finite source degeneracy with no limb darkening
With no limb darkening (i.e. $$\Gamma = 0$$), the maximum change in flux, 

$$\Delta F_{max} = \frac{2F_{s}}{\rho^{2}}.$$

It can be proven that we can factor $$F_{s}, \rho$$ by an arbitrary positive constant, $\zeta$:

$$F_{s}^{\prime} = \zeta F_{s}, \rho^{\prime} = \zeta^{1/2}\rho,$$

and still recover the same change in flux, meaning that in the limit of $$\rho \to \infty$$, 
$$F_{s}$$ and $$\rho$$ are degenerate and 

$$F_{s}^{\prime} = F_{s} \left ( \frac{\rho^{\prime}}{\rho} \right ) ^{2}.$$

The same holds for the blended flux parameter, $$f_{s}$$:

$$f_{s}^{\prime} = f_{s} \left ( \frac{\rho^{\prime}}{\rho} \right )^{2}. $$

Similar arguments can be made for the event duration, $$t_{c} = \beta t_{*}$$.  Substituting $$\beta^{\prime} = \xi \beta$$ 
and $$t_{*}^{\prime} = \xi^{-1}t_{*}$$ results in equivalent chord crossing times for 
any arbirary positive value of $$\xi$$ where $$0 \le \xi\beta \le 1$$. Therefore there is a 
degeneracy between $$b_{0}$$ and $$t_{*}$$ such that:

$$t_{*}^{\prime} = t_{*}\frac{\beta}{\beta^{\prime}} = t_{*}\frac{\sqrt{1 - b_{0}^{2}}}{\sqrt{1 - b_{0}^{\prime 2}}}.$$

Note that these degeneracies are only truly valid when $$\rho \to \infty$$; in the more physical 
case where $$\rho$$ is large but finite, the "shoulders" of the lightcurve will be rounded.  This 
is important because $$f_{ws}$$ is a function of $$\rho$$ but not of $$F_{s}$$, meaning that 
different values of $$\rho$$ produce different lightcurve morphologies.  In addition, since $$f_{ws}$$ 
depends on $$\beta$$ the shape of the lightcurve is also affected by the impact parameter.  As a result, 
observations during these "shoulder" periods are particularly valuable.  

So it is possible to substitute the four observable parameters factored by a constant, $$\eta$$ 
into the expressions above for $$\Delta F_{max}, t_{c}$$ and $$f_{ws}$$:

$$F_{s}^{\prime} = \eta F_{s}, \rho^{\prime} = \eta^{1/2} \rho, \beta^{\prime} = \eta^{-1/4}\beta, t_{*}^{\prime} = \eta^{1/4}t_{*},$$

and recover the same values for those parameters, meaning that the lightcurves are extremely 
similar. 

### Extreme finite source degeneracy including limb darkening
Of course, in reality stars exhibit limb darkening.  For extreme finite source events, this 
means that the morphology of the lightcurve depends not only on $$\rho$$ but also on $$\Gamma$$. 
Since limb darkening relations themselves are a function of radius from the center of the source, 
this introduces a dependence on the impact parameter.  It matters where the chord of the lens' 
trajectory crosses the disk of the source. 

Using a linear limb darkening law, the surface brightness of the source can be described as:

$$S(b(t)) = \left [ 1 - \Gamma \left ( 1 - \frac{3}{2} \sqrt{1 - b^{2}} \right ) \right ],$$

This expression can be parameterized and used to describe the difference in flux as a 
function of time in the presence of limb darkening:

$$ \Delta F(t) = \frac{2F_{s}(1-\Gamma)}{\rho^{2}} \times \left ( 1 + \frac{3\Gamma\beta}{2(1-\Gamma)} T_{c}(t) \right ) H(1 - |\tau_{c}|), $$

where the half-chord crossing time, $$\tau_{c} = (t - t_{0})/t_{c} = \tau_{*}/\beta,$$
and H is a Heaviside step function which represents the different phases of the event:

$$H(x) = 0, x \lt 0; H(x) = \frac{1}{2}, x = 1; H(x) = 1, x \gt 1$$

This can be used to define a shape parameter based on observable characteristics:

$$f_{pl} \equiv \frac{\Delta F(t_{0}) - \Delta F(t_{c})}{\Delta F(t_{0})},$$

which represents the difference between the flux at the peak of the event and that when the lens 
crosses the limb of the source, as a fraction of the peak difference in flux. Combining these 
equations we can infer:

$$f_{pl} = \frac{\frac{3}{2}\Gamma\beta}{(1 - \Gamma) + \frac{3}{2}\Gamma\beta},$$

and the maximum flux difference can be written as:

$$\Delta F_{max} \equiv \frac{2 F_{s}(1 - \Gamma)}{\rho^{2}} \left [ 1 + \frac{f_{pl}}{1 - f_{pl}} \right ].$$

To recap, for a limb darkened source, the peak flux and lightcurve shape depend on $$F_{s}$$, $$\rho$$ and 
$$b_{0}$$.  But the observed duration, $$t_{c}$$ depends on $$t_{*}$$ and also on $$b_{0}$$, so the 
changes in flux and duration are correlated.  

If the limb darkening parameter is fixed, i.e. it can be determined independently of the microlensing 
model, we can explore how $$f_{pl}$$ behaves as a function of $$b_{0}$$ and $$\Gamma$$.  

<figure>
<img src="{{ '/assets/images/johnson2022_fig4.png' | relative_url }}" alt="Fractional peak-to-limb flux difference parameter as a function of b0" style="width:50%;">
  <figcaption>
    The fractional peak-to-limb flux difference parameter as a function of b<sub>0</sub> for values of 
&Gamma; = 0.0, 0.1, 0.2...1.0 (darkest to lightest). [Johnson et al.(2022), Fig. 4]
  </figcaption>
</figure>

This illustrates several points:
* When $$\Gamma = 0, f_{pl} = 0$$, i.e. it is independent of impact parameter when there is no limb darkening;
* With non-zero limb darkening, $$f_{pl}$$ is a weak function of $$b_{0}$$;
* The range of $$b_{0}$$ for which the difference in $$f_{pl}$$ is smaller than a given threshold is
larger for larger $$\Gamma$$, meaning that the lightcurve morphology becomes increasingly 
degenerate for larger values of $$\Gamma$$. 
* For $$\Gamma = 1$$, only three observables can be measured ($$\Delta F_{max}, t_{c}, f_{ws}$$), but 
four parameters are required for the model ($$F_{s}, \rho, \beta, t_{*}$$), so all four parameters 
are degenerate with each other.  



## References
 [Chung et al.(2017) Apj, 838, id.154](https://ui.adsabs.harvard.edu/abs/2017ApJ...838..154C/abstract)<br>
[Gould, A. 1994a ApJ, 421, L71](https://ui.adsabs.harvard.edu/abs/1994ApJ...421L..71G/abstract)<br>
 [Han et al.(2020) AJ, 160, id.64](https://arxiv.org/abs/2003.02375)<br>
[Johnson et al. (2022), ApJ, 927, 24](https://ui.adsabs.harvard.edu/abs/2022ApJ...927...63J/abstract)<br>
 [Liebes, S. (1964), Phys. Rev. 133, 835](https://ui.adsabs.harvard.edu/abs/1964PhRv..133..835L/abstract)<br>
 [Yoo, J., DePoy, D. L., Gal-Yam, A., et al. (2004), ApJ, 603, 139](https://iopscience.iop.org/article/10.1086/381241)