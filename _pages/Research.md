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

Mercury is an odd-ball in the solar system, due to its high core mass fraction (~0.7) opposed to the other rocky planets in the solar system, with core mass fractions (CMFs) of around 0.3. How did Mercury end up with such huge core remains a mystery. One possible theory is that a giant impact has stripped away outer mantle layers from a proto-Mercury, leaving it with a big core mass fraction. However, the probability of a single giant impact with enough energy to strip away so much material is very low. Moreover, observations of volatiles on Mercury's surface challenge this scenario. 

With more and more exoplanets being detected everyday, a number of observations introduce very high density exoplanets. Models of planetary interiors suggest these planets have a Mercury-like composition, however, they are extremely more massive, and have various orbital structures. 

<figure>
  <img src="/images/hypatia.png" alt="Histogram of CMF_stars based on Hypatia">
  <figcaption>Figure 1: By looking at a star's elemental abundances, we can infer the expected cmf of its planets. Looking at the Hypatia catalogue <a href="#ref9">[9]</a> most planets (%95) have an expected CMF between 0.18 and 0.4. This observation makes Mercury and exo-Mercuries extra special!</figcaption>
</figure>

Consequently, understanding Mercury and Exo-Mercury formation is essential to understanding planet formation. In my research, I try to answer questions such as: is it possible to make a Mercury-like planet with a single giant impact? Is it possible to make it with numerous erosive impacts during planetesimal stage? How does the star's metallicity affect the planet compositions? How do differentiating processes affect final planet compositions? What is the role of initial CMF distribution during planetesimal phase?

We do N-body simulations using the state-of-the-art N-body code [rebound](https://github.com/hannorein/rebound) <a href="#ref7">[7]</a> to study the evolution of rocky planets during the planetesimal phase. We start with a disk made of small planetesimals (almost Moon mass) and bigger planetary embryos (~ Mars mass). <a href="#ref1">[1]</a> At this point, all rocky bodies are differentiated. Total disk mass is derived based on the minimum mass solar nebula, and the edges of the disk are based on the solar system rocky planet orbits. Using a [fragmentation module](https://github.com/ANNACRNN/REBOUND_fragmentation/tree/main) <a href="#ref2">[2]</a> we track the composition of bodies during this collision phase. The collision outcome is determined based on the impact energy <a href="#ref3">[3]</a>, which can be erosive producing fragments, accretive, merging or an elastic bounce. We conduct 30 Simulations and integrate for 300 Myrs. 

To study the effects of initial disk composition, or initial core mass fraction distributions, we test the following cases:
1) Uniform CMF distribution, based on solar metallicity
2) Uniform distribution, based on higher metallicity stars
3) Step function CMF distribution, keeping the Iron-mass constant but bringing more Iron to the inner disk (High CMF inner disk and low CMF outer disk)

Our results indicate that without having an Iron-rich region, it is not possible to make a Mercury-like planet and Earth-like planets in the same system.

![grid plot](/images/grid.png)

The table below demonstrates our different choices of initial CMF distributions. 

![cmf_table](/images/cmf_table.jpg)

Previous research has suggested some processes that leads to Iron-enrichment of the inner disk, some of which are magnetic and thermal differentiation. <a href="#ref5">[5]</a><a href="#ref6">[6]</a> Our future steps are to investigate the astrophysical phenomena that are in favor of an Iron-rich inner disk in the planetesimal phase. We also aim to study the probability of forming exo-Mercuries, however to do so we need different disk models, as most exo-Mercuries are much more massive than Mercury (a few Earth mass) and reside in closer orbits to their host star (orbital period in the order of a few days). Having a more massive disk and closer inner edge introduces tremendous computational cost into the simulations, as it will increase particle numbers and will also reduce time step. As fragmentation happens, with more mass there will be more bodies added to the simulation, making the runtime longer and longer. Possible solutions include using a GPU based N-body code or using faster integrators such as TRACE <a href="#ref8">[8]</a>. TRACE supports adding fragments in its newest update, and is expected to be orders of magnitude faster than the current integrator used (MERCURIUS). 

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