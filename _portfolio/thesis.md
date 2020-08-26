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
The percentage of the energy used by data centers for cooling their equipment has been on the rise. With that, there has been a necessity for exploring new and more efficient methods like airside economization, both from an engineering as well as business point of view, to contain this energy demand. Air cooling especially, free air cooling has always been the first choice for IT companies to cool their equipment. But, it has its downside as well. As per  [ASHRAE](https://www.ashrae.org/technical-resources/bookstore/indoor-air-quality-guide) standard (2009b), the air which is entering the data center should be continuously filtered with MERV 11 or preferably MERV 13 filters and the air which is inside the data center should be clean as per ISO class 8. 

The objective of this study is to design a model data center and simulate the flow path with the help of 6sigma room analysis software. A high-density data center was modelled for both hot aisle and cold aisle containment configurations. The particles taken into consideration for modelling were spherical in shape and of diameters 0.05, 0.1 and 1 micron. The physical properties of the submicron particles have been assumed to be same as that of air. For heavier particles of 1 micron in size, the properties of dense carbon particle are chosen for simulating particulate contamination in a data center.

 The Computer Room Air Conditioning unit is modelled as the source for the particulate contaminants which represents contaminants entering along with free air through an air-side economizer. The data obtained from this analysis can be helpful in predicting which type of particles will be deposited at what location based on its distance from the source and weight of the particles. This can further help in reinforcing the regions with a potential to fail under particulate contamination.

## Proceedings Paper


__Paper No__:  IPACK2018-8436, V001T02A011; 12 pages
__DOI__: [10.1115/IPACK2018-8436](https://doi.org/10.1115/IPACK2018-8436)
__Conference__: ASME 2018 International Technical Conference and Exhibition
 on Packaging and Integration of Electronic and Photonic Microsystems
__Published Online__: November 13, 2018

## Problem statement:##
 Analysis on using free-air cooling and identifying the impact of particulate contaminants on the server machines.

 
{% include gallery caption="The various simulations patters observed to go along with this case study." %}

## Computation

CFD modelling is the process of representing a fluid flowproblem  by  mathematical  equations  based  on  the  fundamentallaws of physics, and solving those equations to predict the vari-ation of velocity, pressure and temperature, and other variablessuch as turbulence parameters and concentrations which are dis-ussed by Jone[10].  Eulerian or Lagrangian approaches are oneof the most popular methods for flow visualization and particletracking.   

The difference in both the methods is that the Eule-rian method treats the particles as continuum and the Lagrangianmethods focuses on the particle frame of reference, treating eachparticle individually. Two studies which closely relate to the typeof particle transport model with the present study were by Chenand Zhang[11]which evaluate the flow using RANS (Reynolds Averaged Navier Stokes) and LES (Large Eddy Simulation). Theother study by Seymour[9]used Lagrangian approach, where theassumption that the volume fraction of particles is very less thanthat of total airflow and the particles do not influence the flow of air.  

This describes, more closely, the exact behaviour of partic-ulates in the Data Center space. The fundamental equations that depict the airflow can be expressed as:

$$ \sum F_i = \frac{d(m_p V_i)}{dx} $$

Momentum  force  is  transferred  between  air  and  particlesthrough inter-phase drag and lift forces,  which can be dividedinto, but not limited to, the following parts: the drag force, pres-sure gradient force, unsteady forces which include Basset forceand virtual mass force, Brownian force, and body force, such asgravity force and buoyancy force discussed by Clayton in[12] 

$$ \sum F_i = F_dragi + F_gravi + F_safi + Fbi $$

The drag force on the particle is expressed as, 

$$ F_dragi = -C_D\frac{\pi}{8}\rho d_p^2 $$

... 

## ACKNOWLEDGEMENT

![image-right]({{ site.url }}{{ site.baseurl }}/images/NSF-logo.png){: .align-right}

This  work  is  supported  by  [NSF  IUCRC  Award  No.   IIP-1738811](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1738811&HistoricalAwards=false).
The authors would also like to extend their gratitude to Future Facilities Ltd,
for promptly helping in simulations in 6SigmaRoom CFD Solver.


