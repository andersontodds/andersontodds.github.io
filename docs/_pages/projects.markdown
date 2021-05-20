---
layout: splash
title: "Projects"
permalink: /projects/
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/DSC09368_2.JPG
  caption: Payload 2 undergoing pre-flight tests in Sisters, OR; September 2019
excerpt: ""
---

Broadly speaking, I am interested in the impact of terrestrial and space weather on the Earth's ionosphere and inner magnetosphere.  In my PhD work, I have access to a fantastic dataset of global lightning activity from the World Wide Lightning Location Network (WWLLN), which I help maintain.  I use this dataset--along with data from other instruments we build and deploy, or from existing networks and services--to study the impact of strong solar flares and particle events on radio wave propagation in the Earth-ionosphere waveguide, lightning-launched whistler-mode wave power density in the plasmasphere, and the contribution of global thunderstorms to the Earth's Global Electric Circuit.

**Detection of VLF attenuation in the Earth-ionosphere waveguide associated with solar flares**

Here we used data from the World Wide Lightning Location Network (WWLLN) to observe changes in very low frequency (VLF) radio wave propagation in the Earth-ionosphere waveguide associated with strong solar flares.  VLF radio waves can propagate thousands of kilometers in the waveguide, so WWLLN is able to use a network of spatially-distributed receiving stations to detect radio waves launched by lightning strokes, and thereby locate lightning all over the world.

Solar flares, and other space weather phenomena, alter the plasma density profile of the ionosphere.  Solar flares in particular enhance ionization, and therefore electron density, at low altitudes; driving the bottom-side ionosphere that forms the upper boundary of the Earth-ionosphere waveguide to lower altitude.  Greater neutral atmosphere density at lower altitude means there is more attenuation from electron-neutral collisions, so VLF waves have a harder time propagating long distances through regions of the Earth-ionosphere waveguide impacted by a solar flare.

By assembling a distribution of propagation paths between lightning strokes and WWLLN stations, and observing how this distribution changes in time, we can look for changes in VLF propagation in the Earth-ionosphere waveguide when strong solar flares occur. In **Anderson et al. 2020**, we compared the difference in stroke-station path distribution with HF attenuation modeled by the NOAA D-Region Absorption Prediction (D-RAP) code for the X9.3 and X8.2 flares of September 6-10, 2017. *TODO: add figure from paper comparing WWLLN stroke-station path distribution with D-RAP*

You can find a more detailed description of methods in the paper, and MATLAB code in github.com/andersontodds/pathGrid.  As of November 2020, this repository is not very well streamlined for other users, but I am working on developing a well-documented version with intuitive parameter inputs.  I am also working on a version of this code that can plot attenuation regions in near-real time, updating every 10 minutes.

**Whistler wave density in the plasmasphere from global lightning**

The aim of this project is to get an idea of the overall density of whistler-mode waves in the plasmasphere from global lightning.  Much work has gone into ray-tracing of whistler wave paths in the inner magnetosphere in recent decades, although usually the aim is to correlate satellite observations of particular wave or particle events with specific lightning strokes or other whistler sources.  Here, we will calculate ray paths for all lightning strokes observed in the by WWLLN, and thereby model whistler wave power density from lightning strokes in the plasmasphere.

This project is in its early stages, and is roughly composed of three parts:
 1. modeling wave propagation from a lightning stroke to the top of the ionosphere
 2. ray-tracing waves from the top of the ionosphere into the magnetosphere
 3. modeling wave-particle interactions and energy loss
 
As of November 2020, individual ray paths can be traced from the top of the ionosphere (~1000 km altitude) into the magnetosphere, using Haselgrove's equations.  This ray tracer can be found at github.com/andersontodds/ray-trace.  I am using the [Julia language](https://julialang.org/) for this project, because it is open-source, intuitive, and fast.

**Thunderstorm contribution to the Global Electric Circuit**

Thunderstorms were hypothesized to be the principal driver of the Global Electric Circuit (GEC) nearly 100 years ago by C. T. R. Wilson (1921), but testing this hypothesis has proved difficult due to difficulty in measuring the relative contributions to the GEC of various sources: namely, thunderstorms, electrified shower clouds, and other middle-atmosphere current sources (Williams E. , 2009). This work seeks to quantify the thunderstorm contribution to the GEC by combining two measurement schemes:
 1. A stratospheric balloon campaign, whose payloads will measure vector electric field and electrical conductivity in the fair-weather atmosphere, from which the fair-weather return current of the GEC can be derived, and
 2. A study of global thunderstorm area determined by the World Wide Lightning Location Network (WWLLN), with correction from satellite lightning and cloud imagery.

A test balloon flight was conducted in early September 2019, wherein one payload flew for 31 hours and produced 18.5 hours of usable electric field and conductivity data.  These data were presented in a talk at the 2019 AGU Fall Meeting.  Up to four science flights are planned for Summer 2021.

<figure style="width: 300px" class="align-right">
    <img src="{{ site.url }}{{ site.baseurl }}/assets/images/payload_hangar.jpg">
    <figcaption>One of the payloads being balanced in the hangar.</figcaption>
</figure>

In the banner photo of this page, you can see one of the stratospheric balloon payloads being tested in Sisters, OR, in September 2019.  The tiny white speck above the payload's boom on the right side of the image is the balloon flown during the test flight, catching the last rays of sunlight.
