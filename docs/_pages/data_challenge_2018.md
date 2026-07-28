---
title: "Microlensing Data Challeng 2018"
permalink: /resources/data-challenge-2018/
layout: single
toc: true
toc_label: "On this page"
toc_icon: "list"
sidebar:
  nav: "main"
---

The microlensing community held a data challenge in 2018 with the aim of stimulating research into microlensing modeling in preparation for the Roman Mission.

Historically, the analysis and modeling of microlensing events has always been a computationally-intensive and time-consuming task, requiring a powerful computer cluster as well as well sampled lightcurves.
While the number of interesting events with adequate data remained fairly low, it was practical to perform a careful interactive analysis of each one, often with the aid of a powerful computer cluster,
but modern surveys are expected to produce terabyte and larger scale data products and thousands of
microlensing detections ([Penny et al. 2019](https://ui.adsabs.harvard.edu/abs/2019ApJS..241....3P/abstract), [Johnson et al. 2020](https://ui.adsabs.harvard.edu/abs/2020AJ....160..123J/abstract)) and this approach will not scale. In addition, there are a number of
outstanding challenges in microlensing modeling, particularly concerning the analysis of triple lenses.

The specific goals of the 2018 data challenge were:

* To stimulate research effort into outstanding modeling issues
* To stimulate development of algorithms to detect and classify microlensing events in Roman data
* To stimulate development of software for modeling microlensing events, capable of conducting analyses of Roman-scale datasets

### Data Challenge Logistics
The challenge was coordinated by Rachel Street and centered around a set of simulated lightcurves, produced by Matthew Penny, designed to
reproduce the expected observing cadence, duration and noise model of the Roman Galactic Exoplanet Survey.

The challenge was announced at the annual microlensing meeting in New Zealand, and widely publicized.
The whole community was invited to participate in the challenge, with newcomers to the field especially welcome.
An open [Data Challenge Github Project](https://github.com/microlensing-data-challenge) provided a platform for teams to form and collaborate.

The dataset included lightcurves from non-variable and variable stars, as well as both single and binary microlensing
events of different types, and teams were challenged to identify the nature of the phenomenon causing the
variability in each lightcurve. For microlensing events, they were expected to fit an appropriate model
to the data, and to analyze as much data as possible before the submission deadline, October 31, 2018.

Each entry to the data challenge was required to submit a machine-readable table of fitted model parameters for all lightcurves
in a standardized format to facilitate the programmatic analysis and comparison of the results by
the evaluation panel. No modeling analysis was required for variables, but None entries had to be given rather than missing entries.
For lightcurves classified as microlensing, the appropriate parameters had to be provided with uncertainties, including
binary lens and second-order effect parameters where applicable. This reflects the fact that second-order effects are
not always measurable, so weight was given in the evaluation to constraining the priority parameters well.
The table included the time taken to model each lightcurve, from initial data ingest to final parameter output.

In addition, all entries had to provide written answers to the following questions to provide context which aided in the evaluation of their results.

1. Descriptions of all software used to conduct the analysis, including version numbers where available and all major dependencies (compilers, libraries, external services). This had to include:
   * the algorithm/approach used to classify the lightcurves
   * the algorithm(s) used to find the best-fitting model
   * the algorithm used to evaluate the parameter uncertainties
   * how competing solutions were evaluated and the best fit selected
2. Descriptions of any data filtering or outlier rejection techniques used and any changes made to the photometric errors.
3. If the analysis included limb darkening of the source star, descriptions of the relation or parameterization that was used and the origin of the coefficients.
4. Descriptions of the computer hardware on which the analysis was conducted including number and type of processors (whether GPU or CPU), processor speed, memory, system architecture (e.g. a single multi-processor machine, cluster (Beowulf, condor pool, etc)...) and operating system.

Plots of all fitted lightcurves were encouraged with the model lightcurve overlaid, together with a plot of the lightcurve residuals as a function of time.
Zoomed-in plots of any anomalous features were considered to be advantageous but not required.
Plots of the lens plane geometry, caustic structures and source trajectory were also encouraged.

All entries were evaluated by a panel comprised of experts in microlensing theory and analysis, software and algorithms.
No panel member was allowed to participate in any of the teams and all panel members were required to declare
any conflicts of interest. All submissions were anonymized during the evaluation to minimize unconscious bias, and entries were judged
quantitatively against the input parameters of the simulations.

### Simulated Lightcurve Dataset
The [2018 data challenge dataset](https://github.com/microlensing-data-challenge/data-challenge-1) can be downloaded from here.

The dataset consists of two lightcurve files for each event or star, representing the data from Roman's W149 and Z087 filters.
The files are in ASCII format with the columns BJD, Aperture_Magnitude and Error, and follow the file-naming convention: ulwdc1_nnn_[W149/Z087].txt

Supplementary files are also provided including wfirst_ephemeris.txt, which contains the BJD and 3D spacecraft location within the solar system.
Information is provided on the surface-brightness color relation for Z087-W149 to enable lens masses to be determined where applicable.

It should be noted that in the simulated data, the inertial frame of reference is defined with the x-axis increasing from the binary center of mass towards
the less massive lens at t<sub>0</sub>, the time of closest approach to the center of mass.
If viewed from the solar system barycenter, the inertial frame moves at the relative velocity vlens_CoM &ndash; vobserver(t<sub>0</sub>).
The inclination of the orbit is a counter-clockwise rotation about the x-axis. &alpha; is the angle that the source trajectory
makes with the x-axis (if parallax was 0). Where finite source effects are significant, a linear limb darkening law has been applied.

### Publicly Available Software Tools
A number of software packages for microlensing modeling were made publicly-available to support entrants. Details of these can be found under the
[Software]({{ '/resources/software/' | relative_url }}) page.

Tiffany Meshkat from IPAC kindly developed a Python notebook tutorial which provides an
introduction to three public microlensing packages: PyLIMA, MulensModel and muLAn.
This is a great way to get started if you're new to the field! Click
[here]({{ '/assets/files/challenge_notebook_tutorial.tar' | relative_url }}) to download a tarball of the notebook, data and instructions, or visit the
[IPAC website](https://roman.ipac.caltech.edu/).

### Entries to the 2018 Data Challenge
Four teams entered the 2018 challenge, including 7 people who were newcomers to the field, all of whom were successful in classifying and modeling the dataset using a variety of techniques.

A full overview of the challenge and the results can be found
[here]({{ '/assets/files/2018_microlensing_data_challenge.pdf' | relative_url }})
and was presented at the Roman Science Team Community Briefing in 2021.

<iframe src="{{ '/assets/files/2018_microlensing_data_challenge.pdf' | relative_url }}" width="800" height="900"></iframe>
