---
title: "Path Flow Simulation of  Particulate Contaminants"
excerpt: "Air Flow Pattern and Path Flow Simulation of Airborne Particulate Contaminants in a High-Density Data Center Utilizing Airside Economization "
toc: true
toc_sticky: true
header:
  overlay_image: /images/mountain-2.jpg
  overlay_filter: 0.5
  teaser: images/chip-teaser.jpg
  actions:
    - label: "Paper Link"
      url: "https://doi.org/10.1115/IPACK2018-8436"
sidebar:
  - title: "Gautham Thirunavakkarasu"
    image: /images/headshot.jpg
    image_alt: "logo"
    text: "Graduate Research Assistant, EMNSPC Lab, UTA"
  - title: "Subject Area"
    text: "Flow analysis (dynamics), Predictive Modelling, Flow Simulation"
gallery:
  - url: /images/part-contaminants.jpg
    image_path: images/part-contaminants.jpg
    alt: "Particulate Contaminants"
    title: "Particulate Contaminants"
  - url: /images/trajectory-plot-1m.jpg
    image_path: images/trajectory-plot-1m.jpg
    alt: "Streamline trajectory for 1 micron PC"
    title: "Streamline trajectory for 1 micron PC"
  - url: /images/conc-plot-1m.jpg
    image_path: images/conc-plot-1m.jpg
    alt: "Concentration plot for 1 micron PC"
    title: "Concentration plot for 1 micron PC"
---

August 2018
DOI: [10.1115/IPACK2018-8436](https://doi.org/10.1115/IPACK2018-8436)
Conference: ASME 2018 International Technical Conference and Exhibition
 on Packaging and Integration of Electronic and Photonic Microsystems

Necessity to solve the energy crisis has led to numerous creative solutions. This is
one such method proposed as an alternative to reduce the percentage energy used in
cooling high-density data centers. <br/>

Problem statement: Analysis on using free-air cooling and identifying
 the impact of particulate contaminants on the server machines.

## Summary
Air cooling, especially free air cooling has been a preferred choice for cooling.
But free air, is never void of the numerous elements it contains, such as, moisture,

As per [ASHRAE](https://www.ashrae.org/technical-resources/bookstore/indoor-air-quality-guide) standard (2009b), to ensure a safe and cleaning working environment
for server machines, the air entering the containment must be continuously filtered
with MERV 11 or higher filter which keeps the air clean, per the ISO class 8.

The focus of this study is to simulate the flow pattern of air in different containment
configurations and investigate the particulates that cause contamination and lead to
server failure.The data obtained from this analysis can be used in predicting failure from
contamination and effectively re-designing the containment configuration.

{% include gallery caption="This is a sample gallery to go along with this case study." %}

## Computation
CFD modelling is the process of representing a fluid flowproblem  by  mathematical  equations  based  on  the  fundamentallaws of physics, and solving those equations to predict the vari-ation of velocity, pressure and temperature, and other variablessuch as turbulence parameters and concentrations which are dis-ussed by Jone[10].  Eulerian or Lagrangian approaches are oneof the most popular methods for flow visualization and particletracking.   The difference in both the methods is that the Eule-rian method treats the particles as continuum and the Lagrangianmethods focuses on the particle frame of reference, treating eachparticle individually

## ACKNOWLEDGEMENT

![image-right]({{ site.url }}{{ site.baseurl }}/images/NSF-logo.png){: .align-right}

This  work  is  supported  by  [NSF  IUCRC  Award  No.   IIP-1738811](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1738811&HistoricalAwards=false).
The authors would also like to extend their gratitude to Future Facilities Ltd,
for promptly helping in simulations in 6SigmaRoom CFD Solver.


