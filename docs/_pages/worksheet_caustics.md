---
title: "Caustics"
permalink: /teaching/worksheet-caustics/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

Match the following planetary light curves to their caustics and trajectories. 

* In each light curve identify any caustic entrances and exits and
    look for cusp approaches.
* Also consider when the perturbation occurs: When is the peak of
    the underlying stellar event? Does the planetary perturbation occur
    before or after the peak? 
* Finally, consider the location of the caustic and source
    trajectory: Where is the closest approach between the source and lens
    (where is the source closest to 0,0)? Where is the caustic in relation
    to this?

<table border="1">
  <tr>
    <td>
      <font size="7">1</font>
    </td>
    <td>
      <font size="7">2</font>
    </td>
    <td>
      <font size="7">3</font>
    </td>
    <td>
      <font size="7">4</font>
    </td>
    <td>
      <font size="7">5</font>
    </td>
  </tr>

  <tr>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/OGLE-2007-BLG-368L_Lightcurve.JPG' | relative_url }}" alt="Lightcurve 1" width="200">
          <figcaption>Lightcurve 1 [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/OGLE-2014-BLG-0676L_Lightcurve.JPG' | relative_url }}" alt="Lightcurve 2" width="200">
          <figcaption>Lightcurve 2 [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/MOA-2011-BLG-293L_Lightcurve.JPG' | relative_url }}" alt="Lightcurve 3" width="200">
          <figcaption>Lightcurve 3 [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/MOA-2010-BLG-477L_Lightcurve.JPG' | relative_url }}" alt="Lightcurve 4" width="200">
          <figcaption>Lightcurve 4 [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/MOA-2009-BLG-319L_Lightcurve.JPG' | relative_url }}" alt="Lightcurve 5" width="200">
          <figcaption>Lightcurve 5 [Y.C. Yee]</figcaption>
        </figure>
    </td>
  </tr>
</table>

<table border="1">
  <tr>
    <td>
      <font size="7">A</font>
    </td>
    <td>
      <font size="7">B</font>
    </td>
    <td>
      <font size="7">C</font>
    </td>
    <td>
      <font size="7">D</font>
    </td>
    <td>
      <font size="7">E</font>
    </td>
  </tr>

  <tr>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/MOA-2009-BLG-319L_Caustic.JPG' | relative_url }}" alt="Caustic A" width="200">
          <figcaption>Caustic A [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/OGLE-2014-BLG-0676L_Caustic.JPG' | relative_url }}" alt="Caustic B" width="200">
          <figcaption>Caustic B [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/OGLE-2007-BLG-368L_Caustic.JPG' | relative_url }}" alt="Caustic C" width="200">
          <figcaption>Caustic C [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/MOA-2010-BLG-477L_Caustic.JPG' | relative_url }}" alt="Caustic D" width="200">
          <figcaption>Caustic D [Y.C. Yee]</figcaption>
        </figure>
    </td>
    <td width=300>
        <figure>
          <img src="{{ '/assets/images/MOA-2011-BLG-293L_Caustic.JPG' | relative_url }}" alt="Caustic E" width="200">
          <figcaption>Caustic E [Y.C. Yee]</figcaption>
        </figure>
    </td>
  </tr>
</table>
<button id="AnswerBtn">Answers:</button>
<p id="Answers"> </p>

<script>
document.getElementById("AnswerBtn").addEventListener("click", show_answers)
function show_answers() {
  document.getElementById("Answers").innerHTML = "1) C; <a href='http://adsabs.harvard.edu/cgi-bin/nph-bib_query?bibcode=2010ApJ...710.1641S'>OGLE-2007-BLG-368</a> <br> 2) B; <a href='http://adsabs.harvard.edu/abs/2016arXiv161203511R'>OGLE-2014-BLG-0676</a> <br> 3) E; <a href='http://adsabs.harvard.edu/abs/2012ApJ...755..102Y'>MOA-2011-BLG-293</a> <br>4) D; <a href='http://adsabs.harvard.edu/abs/2012ApJ...754...73B'>MOA-2010-BLG-477</a> <br> 5) A; <a href='http://adsabs.harvard.edu/cgi-bin/nph-bib_query?bibcode=2011ApJ...728..120M'>MOA-2009-BLG-319</a>"
}
</script>