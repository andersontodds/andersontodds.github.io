---
layout: single
title: "Quantifying perpendicularity of a distribution of azimuths"
date: 2022-10-11 17:00:00 -0700
categories: puzzle-solving
hidden: true
header:
    teaser:"{{ site.url }}{{ site.baseurl }}/assets/images/average_paths_202203_smaller.gif"
---

[//]: # Sections:
[//]: #     Motivation
[//]: #     How "pixel" size varies with path density: tic-tac-toe plot
[//]: #     Estimating pixel size when you can't keep track of every path
[//]: #     Paths are not fixed in time
[//]: #     Circular Variance
[//]: #     Perpendicularity: perpendicularity test fig
[//]: #     Apply perpendicularity to WWLLN paths

[//]: # Motivation
One of my current [projects](/projects) is an effort to quantify the spatial scales of energetic electron precipitation (EEP; also called energetic *particle* precipitation, EPP) signatures in the lower ionosphere using the [World Wide Lightning Location Network](https://wwlln.net/) (WWLLN) as an ionosphere remote sensor network.  Current and previous work on EEP detection using subionospheric VLF remote sensing has typically relied on networks of receivers that monitor narrowband transmitters, like the [AARDDVARK network](http://www.physics.otago.ac.nz/space/AARDDVARK_homepage.htm).  These networks are effective because the narrowband transmitter sources have operated reliably for many years, and are thus very well-characterized.  Since the transmitters operate with a continuous carrier frequency, changes in the received signal can be detected at a frequency approaching the Nyquist frequency of the receiver.  Because the transmitters and receivers in VLF networks are usually in fixed positions, the networks consist essentially of a relatively small number of fixed propagation paths that are continuously monitored.



[//]: # Figure template below!
[//]: # <figure class="single" style="width: 400px" class="align-center">
[//]: #     <a href="{{ site.url }}{{ site.baseurl }}/assets/images/average_paths_202203_smaller.gif"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/average_paths_202203_smaller.gif"></a>
[//]: #     <figcaption><i>Click to enlarge!</i> WWLLN stroke-station paths for the month of March 2022, averaged over 10-minute windows in UT. </figcaption>
[//]: # </figure>