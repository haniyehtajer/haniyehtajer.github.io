---
permalink: /research/
title: "Research"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---



Mercury's heart of Iron
----

Mercury is an oddball in the solar system due to its high core mass fraction (~0.7), in contrast to the other rocky planets, which have core mass fractions (CMFs) of around 0.3. How Mercury ended up with such a large core remains a mystery. One possible theory is that a giant impact stripped away the outer mantle layers from a proto-Mercury, leaving it with a large core mass fraction. However, the probability of a single giant impact with enough energy to remove that much material is very low. Moreover, observations of volatiles on Mercury’s surface challenge this scenario.

With more and more exoplanets being detected every day, a growing number of observations have revealed extremely high-density exoplanets. Models of planetary interiors suggest that these planets have Mercury-like compositions; however, they are significantly more massive and exhibit a variety of orbital architectures.

<figure>
  <img src="/images/hypatia.png" alt="Histogram of CMF_stars based on Hypatia">
  <figcaption>Figure 1: By analyzing a star's elemental abundances, we can infer the expected core mass fraction (CMF) of its planets. According to the Hypatia Catalog <a href="#ref9">[9]</a>, most planets (95%) have an expected CMF between 0.18 and 0.4. This makes Mercury and exo-Mercuries extra special!</figcaption>
</figure>

Consequently, understanding the formation of Mercury and exo-Mercuries is essential to understanding planet formation as a whole. In my research, I explore questions such as: Is it possible to form a Mercury-like planet through a single giant impact? Can it instead be produced through multiple erosive impacts during the planetesimal stage? How does a star’s metallicity influence planetary compositions? In what ways do differentiation processes shape a planet’s final composition? And what role does the initial CMF distribution (during the planetesimal phase) play?

We do N-body simulations using the state-of-the-art N-body code [rebound](https://github.com/hannorein/rebound) <a href="#ref7">[7]</a> to study the evolution of rocky planets during the planetesimal phase. We start with a disk made of small planetesimals (almost Moon mass) and bigger planetary embryos (~ Mars mass). <a href="#ref1">[1]</a> At this point, all rocky bodies are differentiated. Total disk mass is derived based on the minimum mass solar nebula, and the edges of the disk are based on the solar system rocky planet orbits. Using a [fragmentation module](https://github.com/ANNACRNN/REBOUND_fragmentation/tree/main) <a href="#ref2">[2]</a> we track the composition of bodies during this collision phase. The collision outcome is determined based on the impact energy <a href="#ref3">[3]</a>, which can be erosive producing fragments, accretive, merging or an elastic bounce. We conduct 30 Simulations and integrate for 300 Myrs. 

We perform N-body simulations using the state-of-the-art [REBOUND N-body code](https://github.com/hannorein/rebound) <a href="#ref7">[7]</a> to study the evolution of rocky planets during the planetesimal phase. We initialize the simulations with a disk composed of small planetesimals (roughly Moon-mass) and larger planetary embryos (~Mars-mass) <a href="#ref1">[1]</a>. At this stage, all rocky bodies are assumed to be differentiated. The total disk mass is based on the minimum-mass solar nebula, and the radial extent of the disk corresponds to the orbital range of the solar system's rocky planets.

Using a [fragmentation module](https://github.com/ANNACRNN/REBOUND_fragmentation/tree/main) <a href="#ref2">[2]</a>, we track the compositional evolution of bodies throughout the collisional phase. Collision outcomes are determined based on impact energy <a href="#ref3">[3]</a>, and can be erosive (producing fragments), accretive, merging, or elastic bounce. We have conducted 30 simulations so far, each integrated for 300 million years.

To study the effects of initial disk composition (initial core mass fraction distributions), we test the following cases:
1) Uniform CMF distribution based on solar metallicity.
2) Uniform distribution based on higher-metallicity stars.
3) Step-function CMF distribution, keeping the total iron mass constant but bringing more iron to the inner disk (high CMF inner disk and low CMF outer disk).

Our results indicate that without having an Iron-rich region, it is not possible to make a Mercury-like planet and Earth-like planets in the same system.

<figure>
    <img src="/images/binned_cmf_a_simple_smoothed.png">
    <figcaption>Figure 2: Regions covered by the evolved planets in our simulations. In simulations with a uniform initial CMF distribution, we observe planets with CMFs as high as 0.4, but none reach Mercury (0.7). However, in the step-function cases, it is possible to produce both Mercury- and Earth-like planets within the same system.
    </figcaption>
</figure>

<figure>
  <img src="/images/grid_magnified.png" alt="Grid plot">
  <figcaption>Figure 3: Plots of semi-major axis vs. CMF for different initial CMF distributions. From left to right, more iron is exchanged between the inner and outer disk. From top to bottom, the boundary between the inner and outer disk is varied, with the highest plots depicting a boundary of 0.5 AU and the lowest ones a boundary of 0.8 AU. The size of the scatter points is scaled to their masses, with the scale illustrated in the top-left plot.</figcaption>
</figure>

The table below demonstrates our different choices of initial CMF distributions. 

<figure>
  <img src="/images/cmf_table.jpg">
  <figcaption>Table 1: Different test cases of initial CMF distribution. We have several step functions, keeping the total iron content of the disk constant. We also test higher total iron contents, based on possible stellar metallicities.
  </figcaption>
</figure> 

Previous research has suggested some processes that lead to iron-enrichment of the inner disk, some of which include magnetic and thermal differentiation <a href="#ref5">[5]</a><a href="#ref6">[6]</a>. Our future steps involve investigating the astrophysical phenomena that favor an iron-rich inner disk during the planetesimal phase. We also aim to study the probability of forming exo-Mercuries; however, to do so, we need different disk models, as most exo-Mercuries are much more massive than Mercury (a few Earth masses) and reside in closer orbits to their host star (orbital periods on the order of a few days). A more massive disk and a closer inner edge introduce tremendous computational costs into the simulations, as they increase the number of particles and reduce the time step. As fragmentation occurs, more mass results in more bodies being added to the simulation, making the runtime longer. Possible solutions include using a GPU-based N-body code or faster integrators, such as TRACE <a href="#ref8">[8]</a>. TRACE supports adding fragments in its newest update and is expected to be orders of magnitude faster than the current integrator used (MERCURIUS).

<h2>References</h2>
<ol>
  <li id="ref1">Chambers, J. et al. (2013). <em>Icarus</em>, 224, 43.</li>
  <li id="ref2">Childs, A. & Steffen, J. (2022). <em>Monthly Notices of the Royal Astronomical Society</em>, 511, 1848.</li>
  <li id="ref3">Leinhardt, Z. M. & Stewart, S. T. (2011). <em>Astrophysical Journal</em>, 745, 79.</li>
  <li id="ref4">Hyodo, R. et al. (2020). <em>Icarus</em>, 354, 114064.</li>
  <li id="ref5">Kruss, M. & Wurm, G. (2018). <em>Astrophysical Journal</em>, 869, 45.</li>
  <li id="ref6">Wurm, G. (2018). <em>Geosciences</em>, 8, 310.</li>
  <li id="ref7">Rein, H. & Liu, S.-F. (2011). <em>Astronomy & Astrophysics</em>, 537, A128.</li>
  <li id="ref8">Lu, T., Hernandez, D. M., & Rein, H. 2024, MNRAS, 533, 3708, <a href="https://doi.org/10.1093/mnras/stae1982" target="_blank">https://doi.org/10.1093/mnras/stae1982</a></li>
  <li id="ref9">Hinkel, N. R., & Burger, D. 2017, <em>arXiv:1712.04944</em></li>
</ol>


<!--
Exo-Mercury detection
-----
Measuring mass and radius of a rocky planet, gives us the bulk density of the planet. Planetary interior models can predict the composition of the planet, based on hydrostatic equilibrium, equations of state, and what we know about the composition of rocky bodies in the solar system. As exoplanet detection techniques become stronger, we are able to detect smaller and smaller planets, introducing some weird planets into the family, with extremely high densities. These planets dubbed "Exo-Mercuries" are predicted to be very Iron-rich, with high core mass fractions (CMFs). 
-->