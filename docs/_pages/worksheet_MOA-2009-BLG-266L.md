---
title: "Worksheet for MOA-2009-BLG-226L"
permalink: /exercises/worksheet-MOA-2009-BLG-226L/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

Event MOA-2009-BLG-226L was first detected on 2009 June 1 by the Microlensing 
Observations in Astrophysics (MOA) survey, using the 1.8m telescope at Mt. John 
University Observatory in New Zealand.  It was then observed intensively by a worldwide 
collaboration of follow-up telescopes.  As a result, the lightcurve was densely sampled 
which allowed a very short-lived planetary anomaly to be detected.  
Analysis of the combined data was published by [Muraki, Y. et al. (2011), ApJ, 741, 22](http://iopscience.iop.org/article/10.1088/0004-637X/741/1/22/pdf).

Use the methods outlined in [estimating parameters](/theory/estimating-parameters/) to 
derive approximate values for the microlensing model parameter. 

<figure>
  <img src="{{ '/assets/images/MOA-2009-BLG-266L_Lightcurve.jpg' | relative_url }}" alt="Lightcurve of MOA-2009-BLG-226L" style="max-width:600px; width:100%;">
  <figcaption>Lightcurve of MOA-2009-BLG-226L [Muraki et al.(2011)]</figcaption>
</figure>

## Determine Parameters of the Underlying Stellar Event 
Based on the microlensing light curve, figure out the following properties of the microlensing event:
<table cellpadding="8">
<tr>
 <th></th>
 <th>Your answers</th>
 <th id="1.0"></th>
</tr>
<tr>
 <td>Time of the peak of the event = t<sub>0</sub>:</td><td> <input type="text"></td><td id="1.1"></td>
</tr>
<tr>
 <td>Change in magnitude $$\Delta m$$</td><td> <input type="text"></td><td id="1.2"></td>
</tr>
<tr>
 <td>Maximum magnification = A<sub>max</sub>:</td><td> <input type="text"></td><td id="1.3"></td>
</tr>
<tr>
 <td>Impact parameter = |u<sub>0</sub>|:</td><td> <input type="text"></td><td id="1.4"></td>
</tr>
<tr>
 <td>Magnitude at Half-Maximum =</td><td> <input type="text"></td><td id="1.5"></td>
</tr>
<tr>
 <td>Full Width Half Maximum = t<sub>FWHM</sub>:</td><td> <input type="text"></td><td id="1.6"></td>
</tr>
<tr>
 <td>Einstein Timescale = t<sub>E</sub>:</td><td> <input type="text"></td><td id="1.7"></td>
</tr>
</table>

<br>
<button id="ex1aBtn">Check</button>

<script>
document.getElementById("ex1aBtn").addEventListener("click", show_ex1a_answers)
function show_ex1a_answers() {
 document.getElementById("1.0").innerHTML = "True answers"
 document.getElementById("1.1").innerHTML = "5093.257 &plusmn; 0.083 "
 document.getElementById("1.4").innerHTML = "0.1315 &plusmn; 0.0008"
 document.getElementById("1.7").innerHTML = "61.47 &plusmn; 0.40"
}
</script>
<br><button id="hint1Btn"> Hint </button><br>
<script>
document.getElementById("hint1Btn").addEventListener("click", show_diagram_hint)
function show_diagram_hint() {
document.getElementById("Hint1.1").style = " "
document.getElementById("Hint1.2").style = " "
}
</script>
<img id="Hint1.1" src="/assets/images/geom_u0t0.png" style="display: none;" width=500>
<img id="Hint1.2" src="/assets/images/geom_FWHM.png" style="display: none;" width=500><br>
<button id="hint2Btn"> Hint 2</button>
<p id="hint2"> </p>

<script>
document.getElementById("hint2Btn").addEventListener("click", show_hint2_content)
function show_hint2_content() {
document.getElementById("hint2").innerHTML ="magnitude<sub>1</sub> - magnitude<sub>2</sub> = - 2.5 log(flux<sub>1</sub>/flux<sub>2</sub>)"
}
</script>
<button id="hint3Btn"> Hint 3 </button>
<p id="hint3"> </p>

<script>
document.getElementById("hint3Btn").addEventListener("click", show_hint3_content)
function show_hint3_content() {
document.getElementById("hint3").innerHTML ="flux<sub>2</sub> = A*flux<sub>1</sub>"
}
</script>

## Determine Parameters of the Planetary Event 

### Step 1: Where is the planet?
<table cellpadding="8">
<tr>
<th></th>
 <th>Your answers</th>
 <th id="2.0"></th>
</tr>
<tr>
 <td>Time of the the planet perturbation = t<sub>planet</sub> :</td><td> <input type="text"></td><td id="2.1"></td>
</tr>
<tr>
 <td>Time scaled to the Einstein timescale = &#964; = |t<sub>planet</sub> - t<sub>0</sub>|/t<sub>E</sub> :</td><td> <input type="text"></td><td id="2.2"></td>
</tr>
<tr>
 <td>Source-lens separation = $$u = \sqrt(u_0^2 + \tau^2)$$</td><td> <input type="text"></td><td id="2.3"></td>
</tr>
<tr>
 <td>$$y_{\pm} = \pm (1/2) (\sqrt(u^2 + 4) \pm u)$$</td><td> <input type="text"></td><td id="2.4"></td>
</tr>
<tr>
 <td>Is the perturbation a major image (+) or minor image (-) perturbation?</td><td> <input type="text"></td><td id="2.5"></td>
</tr>
<tr><td>Location of the planet = s :</td><td> <input type="text"></td><td id="2.6"></td>
</tr>
</table>
<br>

<button id="tut3btn2">Check</button>
<script>
document.getElementById("tut3btn2").addEventListener("click", show_2_answers)
function show_2_answers() {
 document.getElementById("2.0").innerHTML= "True answers"
 document.getElementById("2.6").innerHTML = "0.91434 &plusmn; 0.00036"}
</script>

<br><button id="hint4Btn"> Hint 1</button><br>
<script>
document.getElementById("hint4Btn").addEventListener("click", show_hint4_content)
function show_hint4_content() {
document.getElementById("Hint4.1").style = " "
document.getElementById("Hint4.2").style = " "
document.getElementById("Hint4.3").style = " "
}
</script>
<img id="Hint4.1" src="/assets/images/geom_Aofu.png" style="display: none;" width=500>
<img id="Hint4.2" src="/assets/images/planet_lc_annotated.png" style="display: none;" width=500>
<img id="Hint4.3" src="/assets/images/lensed_images1.png" style="display: none;" width=500><br>
<button id="hint6Btn"> Hint 2</button><br>
<script>
document.getElementById("hint6Btn").addEventListener("click", show_hint)
function show_hint() {
document.getElementById("Hint6.1").style = " "
document.getElementById("Hint6.2").style = " "
document.getElementById("Hint6.3").innerHTML = "<br> A major image perturbation always increases the magnification. In a minor image perturbation, the magnification drops below the expectation for a point lens."
}
</script>
<img id="Hint6.1" src="/assets/images/planet_major.png" style="display: none;" width=500>
<img id="Hint6.2" src="/assets/images/planet_minor.png" style="display: none;" width=500>
<p id="Hint6.3"></p>

### Step 2: What is the mass ratio between the planet and the star? 
<table cellpadding="8">
<tr>
<th></th>
 <th>Your answers</th>
 <th id="3.0"></th>
</tr>
<tr>
 <td>Planet Einstein Timescale = t<sub>p,E</sub> ~ t<sub>FWHM</sub> :</td><td> <input type="text"></td><td id="3.1"></td>
</tr>
<tr>
 <td>Mass Ratio = q = (tp,E / tE)<sup>2</sup>: </td><td> <input type="text"></td><td id="3.2"></td>
</tr>
</table>
<br>
<button id="tut3btn3">Check</button>
<script>
document.getElementById("tut3btn3").addEventListener("click", show_3_answers)
function show_3_answers() {
document.getElementById("3.0").innerHTML = "True answers"
document.getElementById("3.2").innerHTML = "(5.63 &plusmn; 0.25) x10<sup>-5</sup>"
}
</script>

<button id="hint5Btn"> Hint </button>
<p id="hint5"> </p>

<script>
document.getElementById("hint5Btn").addEventListener("click", show_magnitude_hint)

function show_magnitude_hint() {
document.getElementById("Hint5.1").style = " "
}
</script>
<img id="Hint5.1" src="/static/website/planet_lc_annotated.png" style="display: none;" width=500>

<table style="border:1px solid black;<padding: 5px 10px">
<tr> <th>Planet&nbsp;</th>
 <th>&nbsp;&nbsp;&nbsp;&nbsp;q = Planet Mass/Sun's Mass&nbsp;</th>
</tr>
<tr>
 <td>&nbsp;&nbsp;&nbsp;Jupiter&nbsp;</td>
 <td>&nbsp;&nbsp;&nbsp;&nbsp;10<sup>-3</sup>&nbsp;</td>
</tr>
<tr>
 <td>&nbsp;&nbsp;&nbsp;Neptune&nbsp;</td>
 <td>&nbsp;&nbsp;&nbsp;&nbsp;5 x 10<sup>-5</sup>&nbsp;</td>
</tr>
<tr>
 <td>&nbsp;&nbsp;&nbsp;Earth&nbsp;</td>
 <td>&nbsp;&nbsp;&nbsp;&nbsp;3x 10<sup>-6</sup>&nbsp;</td>
</tr>
</table>
<table cellpadding="8">
<tr>
<th></th>
 <th>Your answer</th> <th id="4.0"></th>
</tr>
<tr> <td>Is the planet more similar to Earth, Neptune, or Jupiter?</td><td><input type="text"></td><td id="4.1"></td>
</tr>
</table>

<br>
<button id="tut3btn4">Check</button>
<script>
document.getElementById("tut3btn4").addEventListener("click", show_4_answers)
function show_4_answers() {
document.getElementById("4.0").innerHTML = "True answer"
document.getElementById("4.1").innerHTML = "Neptune"
}
</script>
<hr>

## How well did you do?
Remember that these methods are approximate - they are used to find a good starting point for analysis. 
It's important to remember that the approximation works less well as s--> 1.

IF the light curve is in magnitudes (rather than magnification): We're assuming zero 
blending, i.e. that all the light that you see is from the source star. If there is 
some other (non-lensed) light blended with the light curve, then the true 
magnification is higher. How do your answers change if you assume that half of the 
baseline flux is due to a blend? What if 90% is due to a blend? 

Hint: $$\Delta m = -2.5 log10 [(A*f_s + f_{blend})/(f_s + f_{blend})]$$
