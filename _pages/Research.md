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

Mercury's core mass fraction (CMF) is ~0.7, more than double that of the other rocky planets in the solar system, which have CMFs of ~0.3. The origin of Mercury's large, iron-rich core remains unknown.

Adding to this mystery, an elusive population of “Exo-Mercuries” with high densities is emerging. Therefore, understanding the formation of Mercury and its exoplanetary analogs is essential to developing a comprehensive planet formation theory.

Two hypotheses have been proposed to explain the high CMF of Mercury:

(1) earlier-stage iron enrichment of planetesimals closer to the Sun leads to the formation of an iron-rich planet.

(2) giant impacts during the latest stages of planet formation strip away mantle layers, leaving Mercury with a large core.


<figure>
  <img src="/images/hypo-1-vs-2.png" alt="Hypotheses on Mercury's formation">
  <figcaption>Figure 1: Visualization of hypothesis 1 vs. 2.</figcaption>
</figure>

In this work, we conduct N-body simulations to test these two possibilities. Our simulations are focused on the solar system, however, we aim to provide a framework that can later be applied to the formation of high-CMF exoplanets.

To investigate the giant impact scenario, we employ uniform initial CMF distributions. To address the other hypothesis, we use a step function with higher CMFs in the inner region.

For a uniform initial CMF distribution, our results indicate that although erosive impacts produce iron-rich particles, without mechanisms that deplete stripped mantle material, these particles merge with lower-CMF objects and do not lead to Mercury's elevated CMF. However, a step function initial CMF distribution leads to the formation of a high-CMF planet alongside Earth-like planets, resembling the architecture of the terrestrial solar system.

<figure>
  <img src="/images/cham_cont_animation.gif" alt="Hypotheses on Mercury's formation">
  <figcaption>Figure 2: Evolution of planets through N-body simulations. The left plot starts from a uniform, Earth-like composition disk, and the right plot starts from a planetesimal disk with an Iron-rich inner region.</figcaption>
</figure>


If you are interested in this work, checkout [my paper!](https://arxiv.org/abs/2511.01842)



<!--
Exo-Mercury detection
-----
Measuring mass and radius of a rocky planet, gives us the bulk density of the planet. Planetary interior models can predict the composition of the planet, based on hydrostatic equilibrium, equations of state, and what we know about the composition of rocky bodies in the solar system. As exoplanet detection techniques become stronger, we are able to detect smaller and smaller planets, introducing some weird planets into the family, with extremely high densities. These planets dubbed "Exo-Mercuries" are predicted to be very Iron-rich, with high core mass fractions (CMFs). 
-->