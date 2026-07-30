---
title: "Single Lens Simulator"
permalink: /resources/single-lens-simulator/
layout: single
classes: wide
---

[&larr; Back to Simulators]({{ '/resources/simulators/' | relative_url }})

<div><h5>By Shanen Cross</h5></div>
<div style="text-align:center;">For best performance, please use Chrome or Safari.  Firefox is somewhat slower, and IE lacks some of the necessary functions</div>

<div class="row" style="width:100%; max-width:1200px; margin-left:auto; margin-right:auto; position:relative;">
  <canvas id="lcurveCanvas" style="float:left; border:1px solid #d8dee1; border-radius:10px; max-width:48%; height:auto;" width="550" height="400">
  Your browser does not support HTML5 canvas. Please use a compatible browser.
  </canvas>
  <canvas id="lensPlaneCanvas" style="margin-left:10px; border:1px solid #d8dee1; border-radius:10px; max-width:48%; height:auto;" width="550" height="400">
  </canvas>
</div>

<div style="text-align:center; position:relative;">
  <input type="button" id="stepBack" value="&#9194;">
  <input type="button" id="play" value="&#9654;">
  <input type="button" id="pause" value="&#9646;&#9646;">
  <input type="button" id="stepForward" value="&#9193;">
  <input type="button" id="timeReset" value="Reset">
</div>

<div class="row" style="text-align:center; position:relative; padding: 5px 10px; justify-content:center;">
  <div>Time: <span id="timeReadout">-16.0000</span> days</div>
  <div>&theta;<sub>E</sub>: <span id="thetaEreadout">0.1206</span> mas</div>
  <div>&theta;<sub>x</sub>: <span id="thetaXreadout">0.3066</span> mas</div>
  <div>&rho;: <span id="sourceRadiusNormalizedReadout">0.1105</span></div>
  <div><input type="checkbox" id="fixU0checkbox">Hold u0 fixed when changing other quantities</div>
  <div><input type="checkbox" id="displayImagesCheckbox" checked>Display images</div>
  <div><input type="checkbox" id="displayRingsCheckbox" checked>Display Einstein ring</div>
</div>

<div style="width:100%; max-width:1200px; padding: 5px 10px; text-align:center;">
  <table style="width:100%; max-width:900px; margin-left:auto; margin-right:auto; border:1px solid #d8dee1; border-radius:10px; overflow:hidden;">
    <tr>
      <td valign="top" style="width:450px; background-color:#f4f7f8;padding:10px"><h3>Event Parameters</h3>
        <table style="width:100%;">
          <tr>
            <td>Einstein crossing time, t<sub>E</sub></td>
            <td style="width:60%;"><input type="range" id="tEslider" min="0.001" max="365" step="0.001" value="6.293" style="width:100%;">
            <span id="tEreadout" style="display:inline-block; width:3.8em; text-align:right;">6.293</span> days</td>
          </tr>
          <tr>
            <td>Impact parameter, u<sub>0</sub><br>[units of &theta;<sub>E</sub>]</td>
            <td style="width:60%;"><input type="range" id="u0slider" min="-2" max="2" step="0.001" value="0.1" style="width:100%;">
            <span id="u0readout" style="display:inline-block; width:2.3em; text-align:right;">0.100</span></td>
          </tr>
          <tr>
            <td>Time of peak, t<sub>0</sub></td>
            <td style="width:60%;"><input type="range" id="t0slider" min="-75" max="75" step="0.1" value="0" style="width:100%;">
            <span id="t0readout" style="display:inline-block; width:2.3em; text-align:right;">0.0</span> days</td>
          </tr>
          <tr>
            <td>Lens-source relative<br>proper motion, &mu;<sub>rel</sub></td>
            <td style="width:60%;"><input type="range" id="muSlider" min="0.01" max="10" step="0.01" value="7" style="width:100%;">
            <span id="muReadout" style="display:inline-block; width:2.3em; text-align:right;">7.00</span> mas/yr</td>
          </tr>
        </table>
        <h3>Relative trajectory</h3>
        <table style="width:100%;">
          <tr>
            <td>Impact parameter, &theta;<sub>y</sub></td>
            <td style="width:60%;"><input type="range" id="thetaYslider" min="-2" max="2" step="0.001" value="0.012" style="width:100%;">
            <span id="thetaYreadout" style="display:inline-block; width:2.6em; text-align:right;">0.012</span> mas</td>
          </tr>
        </table>
      </td>

      <td valign="top" style="width:450px; background-color:#f4f7f8;padding:10px"><h3>Physical Parameters</h3>
        <table style="width:100%;">
          <tr>
            <td>Lens mass, M<sub>l</sub></td>
            <td style="width:60%;"><input type="range" id="MlSlider" min="0.000001" max="15" step="0.000001" value="0.1" style="width:100%;">
            <span id="MlReadout" style="display:inline-block; width:4.8em; text-align:right;">0.100000</span> M<sub>&#9737;</sub></td>
          </tr>
          <tr>
            <td>Source distance, D<sub>s</sub></td>
            <td style="width:60%;"><input type="range" id="DsSlider" min="0.01" max="8.5" step="0.01" value="8.0" style="width:100%;">
            <span id="DsReadout" style="display:inline-block; width:2.3em; text-align:right;">8.00</span> kpc</td>
          </tr>
          <tr>
            <td>Lens distance, D<sub>l</sub></td>
            <td style="width:60%;"><input type="range" id="DlSlider" min="0.01" max="8.5" step="0.01" value="7" style="width:100%;">
            <span id="DlReadout" style="display:inline-block; width:2.3em; text-align:right;">7.00</span> kpc</td>
          </tr>
        </table>
        <table style="width:100%;">
          <tr>
            <td><a id="toggleLink" href="" onclick="return false;" style="display:block; padding-top:10px">+ Show Options For Finite Source Effects</a></td>
          </tr>
          <tbody id="toggledElement" style="display:none;">
            <tr>
              <td colspan="2"><input type="checkbox" id="finiteSourceCheckbox">Use finite source</td>
            </tr>
            <tr>
              <td>source radius</td>
              <td style="width:60%;"><input type="range" id="sourceRadiusSlider" min="0.0001" max="0.5000" step="0.001" value="0.0133" style="width:100%;">
              <span id="sourceRadiusReadout" style="display:inline-block; width:3.8em; text-align:right;">0.0133</span> mas</td>
            </tr>
          </tbody>
          <tr valign="bottom">
            <td valign="bottom" style="padding-top: 10px"><input type="button" id="resetParams" value="Reset Parameters"></td>
          </tr>
        </table>
      </td>
    </tr>
  </table>
</div>

<div style="width:100%; max-width:1200px; padding: 5px 10px; text-align:center;">
  <table style="width:100%; max-width:900px; margin-left:auto; margin-right:auto; border:1px solid #d8dee1; border-radius:10px; overflow:hidden;">
    <tr style="background-color:#f4f7f8;">
      <td valign="top" colspan="5"><h4>Plotting range controls</h4></td>
    </tr>
    <tr style="background-color:#f4f7f8; text-align:center;">
      <td style="width:180px;"><input type="button" id="xLeft" value="x<--">
      <input type="button" id="xRight" value="x-->"></td>
      <td style="width:180px;"><input type="button" id="xZoomIn" value="x+">
      <input type="button" id="xZoomOut" value="x-"></td>
      <td style="width:180px;"><input type="button" id="yUp" value="y ^">
      <input type="button" id="yDown" value="y v"></td>
      <td style="width:180px;"><input type="button" id="yZoomIn" value="y+">
      <input type="button" id="yZoomOut" value="y-"></td>
      <td style="width:180px;"><input type="button" id="resetGraph" value="Reset Range/Scale"></td>
    </tr>
  </table>
</div>

<script src="{{ '/assets/js/FSPL_bundle.js' | relative_url }}"></script>
