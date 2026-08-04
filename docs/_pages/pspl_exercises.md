---
title: "PSPL Exercises"
permalink: /teaching/pspl-exercises/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
You can learn a great deal about a microlensing event from it's lightcurve.  
As we discussed in [estimating parameters](/theory/estimating-parameters/), you 
can approximately measure the key parameters quite simply.  These exercises 
help to practise this technique.

## Understanding the impact parameter
In the limit that u<sub>0</sub> << 1, what is A(u)?

<button id="afnBtn">Answer</button>
<p id="afnAns"> </p>

<script>
document.getElementById("afnBtn").addEventListener("click", show_mag_limit)

function show_mag_limit() {
  document.getElementById("afnAns").innerHTML = "A(u) ~ 1/u<sub>0</sub>"
}
</script>

## Example Events
Below are discovery lightcurves of the first microlensing events. For
each one, estimate its point lens parameters (t<sub>0</sub>, u<sub>0</sub>, 
t<sub>E</sub>). These basic parameters can be directly inferred from the 
lightcurve by measuring the height and time of the peak and t<sub>FWHM</sub> of
the lightcurve (FWHM = Full Width Half Maximum). Then, t<sub>E</sub>
can be calculated using the measured t<sub>FWHM</sub> and the above
equations. In the limit where <i>u</i><sub>0</sub> << 1, t<sub>E</sub>
~ (1/2)t<sub>FWHM</sub>/<i>u</i><sub>0</sub>. 

<table>
<tr>
<td>
<figure>
  <img src="{{ '/assets/images/geom_u0t0.png' | relative_url }}" alt="Estimating t0 and u0 for a point source, point lens event" width="200">
  <figcaption>Estimating t0 and u0 for a point source, point lens event [Y.C. Yee]</figcaption>
</figure>
</td>
<td>
<figure>
  <img src="{{ '/assets/images/geom_FWHM.png' | relative_url }}" alt="Estimating tE for a point source, point lens event" width="200">
  <figcaption>Estimating tE for a point source, point lens event [Y.C. Yee]</figcaption>
</figure>
</td>
</tr>
</table>

### The first MACHO event
In 1993, the MACHO survey announced it's first microlensing discovery in the paper 
[Alcock et al (1993)](http://www.nature.com/nature/journal/v365/n6447/abs/365621a0.html).  
Use their lightcurve (below) to estimate the main parameters for that event.  

<figure>
  <img src="{{ '/assets/images/Alcock_etal_1993_Fig2.png' | relative_url }}" alt="Lightcurve of MACHO-1" width="200">
  <figcaption>Lightcurve of MACHO-1 [Alcock et al. Figure 2]</figcaption>
</figure>

<table>
<tr>
  <th></th>
  <th>Your answers</th>
  <th id="ex1head"></th>
</tr>
<tr>
  <td>t<sub>0</sub>:</td><td> <input type="text"></td><td id="ex1t0"></td>
</tr>
<tr>
  <td>u<sub>0</sub>:</td><td> <input type="text"></td><td id="ex1u0"></td>
</tr>
<tr>
  <td>t<sub>E</sub>:</td><td> <input type="text"></td><td id="ex1tE"></td>
</tr>
</table>

<button id="ex1Btn">Check</button>

<script>
document.getElementById("ex1Btn").addEventListener("click", show_ex1_answers)

function show_ex1_answers() {
  document.getElementById("ex1head").innerHTML = "True answers"
  document.getElementById("ex1t0").innerHTML = "433.55 &plusmn; 0.04 d"
  document.getElementById("ex1u0").innerHTML = "0.147"
  document.getElementById("ex1tE").innerHTML = "33.9 &plusmn; 0.26 d"
}
</script>

### The First EROS Events
The EROS survey also published their first discoveries in 1993, in a paper by 
[Aubourg et al. (1993)](http://www.nature.com/nature/journal/v365/n6447/abs/365623a0.html). 
Estimate the parameters for these events from the lightcurves below. 

<figure>
  <img src="{{ '/assets/images/Aubourg_etal_1993_Fig1b.png' | relative_url }}" alt="Lightcurve of EROS-1" width="200">
  <figcaption>Lightcurve of the first EROS event [Aubourg et al. Figure 1b]</figcaption>
</figure>


<button id="hintBtn"> Hint 1 </button>
<p id="hint"> </p>

<script>
document.getElementById("hintBtn").addEventListener("click", show_magnitude_hint)

function show_magnitude_hint() {
  document.getElementById("hint").innerHTML ="magnitude<sub>1</sub> - magnitude<sub>2</sub> = - 2.5 log(flux<sub>1</sub>/flux<sub>2</sub>)"
}
</script>


<button id="hint2Btn"> Hint 2 </button>
<p id="hint2"> </p>

<script>
document.getElementById("hint2Btn").addEventListener("click", show_magnitude_hint)

function show_magnitude_hint() {
  document.getElementById("hint2").innerHTML ="flux<sub>2</sub> = A*flux<sub>1</sub>"
}
</script>

<table>
<tr>
  <th></th>
  <th>Your answers</th>
  <th id="ex2ahead"></th>
</tr>
<tr>
  <td>t<sub>0</sub>:</td><td> <input type="text"></td><td id="ex2at0"></td>
</tr>
<tr>
  <td>u<sub>0</sub>:</td><td> <input type="text"></td><td id="ex2au0"></td>
</tr>
<tr>
  <td>t<sub>E</sub>:</td><td> <input type="text"></td><td id="ex2atE"></td>
</tr>
</table>

<button id="ex2aBtn">Check</button>

<script>
document.getElementById("ex2aBtn").addEventListener("click", show_ex2a_answers)

function show_ex2a_answers() {
  document.getElementById("ex2ahead").innerHTML = "True answers"
  document.getElementById("ex2at0").innerHTML = "761 d"
  document.getElementById("ex2au0").innerHTML = "0.425"
  document.getElementById("ex2atE").innerHTML = "27 &plusmn; 2 d"
}
</script>

<figure>
  <img src="{{ '/assets/images/Aubourg_etal_1993_Fig2b.png' | relative_url }}" alt="Lightcurve of EROS-2" width="200">
  <figcaption>Lightcurve of the second EROS event [Aubourg et al. Figure 2b]</figcaption>
</figure>

<table>
<tr>
  <th></th>
  <th>Your answers</th>
  <th id="ex2bhead"></th>
</tr>
<tr>
  <td>t<sub>0</sub>:</td><td> <input type="text"></td><td id="ex2bt0"></td>
</tr>
<tr>
  <td>u<sub>0</sub>:</td><td> <input type="text"></td><td id="ex2bu0"></td>
</tr>
<tr>
  <td>t<sub>E</sub>:</td><td> <input type="text"></td><td id="ex2btE"></td>
</tr>
</table>

<button id="ex2bBtn">Check</button>

<script>
document.getElementById("ex2bBtn").addEventListener("click", show_ex2b_answers)

function show_ex2b_answers() {
  document.getElementById("ex2bhead").innerHTML = "True answers"
  document.getElementById("ex2bt0").innerHTML = "362 d"
  document.getElementById("ex2bu0").innerHTML = "0.346"
  document.getElementById("ex2btE").innerHTML = "30 &plusmn; 3 d"
}
</script>

## Conclusions
In each of the examples shown above, there are two panels shown: red
and blue. Why? Gravitational lensing is <i>achromatic</i> meaning that
all light is magnified equally, regardless of wavelength. The fact
that the lensing signal is the same in both bands is further proof
that the observed light curves are caused by lensing rather than some
other astrophysical effect. (For example, a stellar flare would look
different in red and blue light.) The bottom panel of the first
figure, A<sub>red</sub>/A<sub>blue</sub>, demonstrates that the signal
is achromatic by showing that the ratio of the magnifications is flat.


## References
[Alcock, Akerlof, Allsman, et al. 1993 Nature, 365, 621](http://www.nature.com/nature/journal/v365/n6447/abs/365621a0.html)<br>
[Aubourg, Bareyre, Br&eacute;hin, et al. 1993 Nature, 365, 623](http://www.nature.com/nature/journal/v365/n6447/abs/365623a0.html)