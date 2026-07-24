---
title: "Caustics"
permalink: /theory/caustics/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

## Introduction
In microlensing, the <b>caustic</b> corresponds to the position(s) of the
source for which the solution of the lens equation results in infinite
magnification. For a point lens (e.g. a single star), the magnification (A) equation is:
$$A = \frac{u^{2} + 2}{u(u^2 + 4)^{1/2}}$$, 
where u is the source positions. If you solve this equation for u=0,
you will find that the magnification, A, is infinite. Thus, for a
point lens, the caustic is a single point at u=0.

For a 2-body lens (such as a star+planet), the magnification equation
is more complex, but it remains true that there are solutions to this
equation for which the magnification is infinite. In this case, the
caustic is a closed curve, or set of closed curves, and at those
curves the magnification diverges to infinity.

By solving the lens equation, it is possible to calculate the
magnification of the source at any (projected) position relative to
the position of the lens. The <b>magnification map</b> is a
visualization reflecting the calculated magnification at a given point
(brighter=more highly magnified). The image below shows the
magnification map and caustic structure for a 2-body lens.

<TABLE WIDTH="30%">
<TR>
  <td align="center">Magnification Map</td>
  <td align="center">Caustic</td>
  <td align="center">Magnifcation Map & Caustic </td>
</tr>
<tr>
  <TD WIDTH="10%" ALIGN="left" VALIGN="bottom">
<figure>
  <img src="{{ '/assets/images/magnification_map1.gif' | relative_url }}" alt="Magnification map" width="200">
  <figcaption>Magnification map [Y.C. Yee]</figcaption>
</figure>
 </TD>
  <TD WIDTH="10%" ALIGN="left" VALIGN="bottom">
<figure>
  <img src="{{ '/assets/images/caustic1.gif' | relative_url }}" alt="Caustic" width="200">
  <figcaption>Caustic [Y.C. Yee]</figcaption>
</figure>
 </TD>
  <TD WIDTH="10%" ALIGN="left" VALIGN="bottom">
<figure>
  <img src="{{ '/assets/images/Jennifer_Yee__map_animation.gif' | relative_url }}" alt="Magnification map and caustic" width="200">
  <figcaption>Magnification map and caustic [Y.C. Yee]</figcaption>
</figure>
  </TD>
</TR>
</TABLE>

## Some general rules about caustics
* They are closed curves. Therefore, they have an inside and an
outside. (The perimeter of a square or a triangle are other examples
of closed curves. But remember that the caustic refers to the edge of
the shape and not the shape itself.)
<figure>
  <img src="{{ '/assets/images/caustic_inout.jpg' | relative_url }}" alt="Caustic description" width="200">
  <figcaption>Caustic description [Y.C. Yee]</figcaption>
</figure>
* The caustic has zero width. (A mathematical line also has
zero width.)
* The magnification diverges to infinity  at the caustic.
* The magnification inside of the caustic is always greater than the
magnification outside of the caustic.
* The points of a caustic are called <b>cusps</b>. The curved segments
connecting the cusps are called <b>folds</b>
<figure>
  <img src="{{ '/assets/images/caustic_annotated.jpg' | relative_url }}" alt="Annotated caustic" width="200">
  <figcaption>Annotated caustic [Y.C. Yee]</figcaption>
</figure>

## How do caustics relate to light curve features?
The following animation shows what happens when a source crosses
into a caustic (aka a <b>caustic entrance</b>):
<figure>
  <img src="{{ '/assets/images/caustic_entrance.gif' | relative_url }}" alt="Caustic entrance" width="200">
  <figcaption>Caustic entrance [Y.C. Yee]</figcaption>
</figure>

There is a sharp jump in magnification when the source crosses into
the caustic (red). Once inside the caustic, the magnification declines but
always stays above the level outside the caustic.

A <b>caustic exit</b> is the inverse of a caustic entrance: the
magnification increases as the source approaches the caustic, then
drops abruptly when the source crosses outside the caustic.

<figure>
  <img src="{{ '/assets/images/caustic_exit.gif' | relative_url }}" alt="Caustic exit" width="200">
  <figcaption>Caustic exit [Y.C. Yee]</figcaption>
</figure>

Because the caustic is a closed curve, there will always be two
caustic crossings: an entrance and an exit. The figure below shows the
magnification curve for a source crossing the caustic of a binary star
lens. Can you identify the caustic entrance and the caustic exit in
the light curve?

The caustic structure is often used as a kind of short-hand for the
full magnification map because the features of the magnification map
can be inferred from the caustic structure. Recall that a cusp is one
of the points of the caustic. The animation below shows how the
magnification is increased near the cusps.

<figure>
  <img src="{{ '/assets/images/Jennifer_Yee__map_animation_cropped.gif' | relative_url }}" alt="Animation of a magnification map and caustic" width="200">
  <figcaption>Animation of a magnification map and caustic [Y.C. Yee]</figcaption>
</figure>

A source passing near a cusp can produce a magnified signal without
actually crossing the caustic directly:

<figure>
  <img src="{{ '/assets/images/caustic_cusp.gif' | relative_url }}" alt="Caustic cusp" width="200">
  <figcaption>Caustic cusp [Y.C. Yee]</figcaption>
</figure>

Notice the single peak and rounded form of the <b>cusp
approach</b>. A <b>cusp crossing</b> may also appear to be a single
peak if the distance between the cusps is smaller than the diameter of
the source. In that case, the caustic entrance and exit merge,
producing a single peak but with sharp, rather than smooth shoulders.

## Caustics and Finite Source Effects
At a caustic, the mathematical solution to the lens equation gives
infinite magnification, but infinite magnification is never observed
in practice. Why?

When evaluating the lens equation, we get infinite magnification if
we assume the source is a point source, meaning that it is a
mathematical point with zero size. In reality, the sources are stars,
which have a physical size and therefore a finite extent. The observed
magnification of the source is smeared out by the face of the
source. If you wear glasses, this is similar to how things appear
blurry if there is a smudge on the glasses. In practice we calculate
the magnification of a source by integrating the magnification pattern
across the face of the source.

The animation below compares a caustic entrance for a point source
(dotted line) to a source with radius 0.01.

<figure>
  <img src="{{ '/assets/images/Jennifer_Yee__fs_effects.gif' | relative_url }}" alt="The effects of a finite source on caustics" width="200">
  <figcaption>The effects of a finite source on caustics [Y.C. Yee]</figcaption>
</figure>

If you are familiar with transiting planet lightcurves, this effect
is directly analogous to the points of first and second contact for a
transit. The images below show a caustic entrance and the first and
second points of contact and a caustic exit and the third and
fourth points of contact.


<figure>
  <img src="{{ '/assets/images/pts_of_contact_0.png' | relative_url }}" alt="Points of contact with a caustic" width="200">
  <img src="{{ '/assets/images/pts_of_contact_1.png' | relative_url }}" alt="Points of contact with a caustic" width="200">
  <figcaption>Points of contact with a caustic [Y.C. Yee]</figcaption>
</figure>
