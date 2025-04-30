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

Consequently, understanding Mercury and Exo-Mercury formation is essential to understanding planet formation. In my research, I try to answer questions such as: is it possible to make a Mercury-like planet with a single giant impact? Is it possible to make it with numerous erosive impacts during planetesimal stage? How does the star's metallicity affect the planet compositions? How do differentiating processes affect final planet compositions? What is the role of initial CMF distribution during planetesimal phase?

We do N-body simulations using the state-of-the-art N-body code [rebound](https://github.com/hannorein/rebound) to study the evolution of rocky planets during the planetesimal phase. We start with a disk made of small planetesimals (almost Moon mass) and bigger planetary embryos (~ Mars mass). At this point, all rocky bodies are differentiated. Total disk mass is derived based on the minimum mass solar nebula, and the edges of the disk are based on the solar system rocky planet orbits. Using a [fragmentation module](https://github.com/ANNACRNN/REBOUND_fragmentation/tree/main) we track the composition of bodies during this collision phase. The collision outcome is determined based on the impact energy, which can be erosive producing fragments, accretive, merging or an elastic bounce. We conduct 30 Simulations and integrate for 300 Myrs. 

To study the effects of initial disk composition, or initial core mass fraction distributions, we test the following cases:
1) Uniform CMF distribution, based on solar metallicity
2) Uniform CMF distribution, based on higher metallicity stars
3) Step function CMF distribution, keeping the Iron-mass constant but bringing more Iron to the inner disk (High CMF inner disk and low CMF outer disk)

Our results indicate that without having an Iron-rich region, it is not possible to make a Mercury-like planet and Earth-like planets in the same system.

![grid plot](/images/grid.png)

ADD TABLE


ADD RESULTS


Exo-Mercury detection
-----
Measuring mass and radius of a rocky planet, gives us the bulk density of the planet. Planetary interior models can predict the composition of the planet, based on hydrostatic equilibrium, equations of state, and what we know about the composition of rocky bodies in the solar system. As exoplanet detection techniques become stronger, we are able to detect smaller and smaller planets, introducing some weird planets into the family, with extremely high densities. These planets dubbed "Exo-Mercuries" are predicted to be very Iron-rich, with high core mass fractions (CMFs). 