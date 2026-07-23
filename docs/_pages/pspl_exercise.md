---
title: "PSPL Exercise"
permalink: /exercises/pspl-exercise/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

This exercise illustrates the core concepts of point source, point lens events.  
It was developed by Y.C. Yee.

## The First Microlensing Events

Below are discovery lightcurves of the first microlensing events. For
each one, estimate its point lens parameters (t<sub>0</sub>, u<sub>0</sub>, t<sub>E</sub>). These basic parameters can be directly inferred from the lightcurve
by measuring the height and time of the peak and t<sub>FWHM</sub> of
the lightcurve (FWHM = Full Width Half Maximum). 

### MACHO-1
Published in [Alcock, Akerlof, Allsman, et al. (1993), Nature, 365, 621](http://www.nature.com/nature/journal/v365/n6447/abs/365621a0.html).

<figure>
  <img src="{{ '/assets/images/Alcock_etal_1993_Fig2.png' | relative_url }}" alt="Lightcurve of microlensing event MACHO-1." style="max-width:400px; width:50%;">
  <figcaption>Lightcurve of MACHO-1, Alcock et al. Figure 2 [Alcock et al. (1993)]</figcaption>
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

### EROS-1
From [Aubourg, Bareyre, Bréhin, et al. 1993 Nature, 365, 623](http://www.nature.com/nature/journal/v365/n6447/abs/365623a0.html)

<figure>
  <img src="{{ '/assets/images/Aubourg_etal_1993_Fig1b.png' | relative_url }}" alt="Lightcurve of microlensing event EROS-1." style="max-width:400px; width:50%;">
  <figcaption>Lightcurve of the first EROS event, Aubourg et al. Figure 1b [Aubourg et al. (1993)]</figcaption>
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

### EROS-2
Also from [Aubourg, Bareyre, Bréhin, et al. 1993 Nature, 365, 623](http://www.nature.com/nature/journal/v365/n6447/abs/365623a0.html)

<figure>
  <img src="{{ '/assets/images/Aubourg_etal_1993_Fig2b.png' | relative_url }}" alt="Lightcurve of microlensing event EROS-2." style="max-width:400px; width:50%;">
  <figcaption>Lightcurve of the second EROS event, Aubourg et al. Figure 2b [Aubourg et al. (1993)]</figcaption>
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

## Discussion
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
[Alcock, Akerlof, Allsman, et al. (1993), Nature, 365, 621](http://www.nature.com/nature/journal/v365/n6447/abs/365621a0.html)<br>
[Aubourg, Bareyre, Bréhin, et al. 1993 Nature, 365, 623](http://www.nature.com/nature/journal/v365/n6447/abs/365623a0.html)
