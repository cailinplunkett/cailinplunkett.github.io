---
layout: research
title: Research
permalink: /research/
main_nav: true
---

<section class="research-intro">
  <h1>Research</h1>
  <p>I study <strong>binary black holes</strong> using <strong>gravitational waves</strong>—ripples in spacetime that encode the masses, spins, and orientations of merging compact objects. My goal is to understand the <strong>astrophysical origins</strong> of the black holes observed by LIGO–Virgo–KAGRA and link our observations to theories of stellar evolution. The size and complexity of our dataset also requires state-of-the-art statistical methods to glean insight. I aim to develop <em>efficient</em>, <em>flexible</em> data-analysis tools and <em>stress-test</em> our model assumptions.</p>
</section>

<section class="research-channels">
  <h2>Formation Channels</h2>
  <p> One of the major questions in gravitational-wave astrophysics is <em> how do we get two black holes close enough to merge in the first place? </em> </p>
  <p>Much of my work engages with this question in some capacity, from devising machine-learning methods to link stellar evolution simulations with observed black holes, to careful modeling of black hole spins to tease out distinct subpopulations in the data. </p>
  <p>There are two main classes of models for how merging binary black holes form. In <em>isolated evolution</em>, two stars are born together and co-evolve over their lifetimes, often exchanging mass (and drawing closer) through interactions like common envelope evolution. In <em>dynamical formation</em>, encounters in dense stellar clusters promote binary formation and mergers; if a merger remnant is retained in the cluster, it can merge again—producing so-called <em>hierarchical mergers</em>. These two channels have distinct, yet overlapping, predictions for the distributions of black hole masses, spins, and redshifts.</p>
  <p> We typically expect isolated black hole binaries to be <em> slowly rotating </em> and <em> aligned </em> with the orbital angular momentum. Cluster binaries formed by dynamical capture are thought to have no preferred direction, but rather an <em> isotropic </em> distribution of black hole spin directions, though we still expect small spin magnitudes from black holes born directly from stellar collapse. A <em>second-generation</em> black hole formed from a previous merger changes this picture: these are likely <em>rapidly rotating</em> at typically ~70% of the possible maximum. </p>
  <p>These different spin signatures offer footholds to identify these distinct formation histories in the data. However, unfortunately, these quantities are difficult to measure. Principled statistical modeling, and caution against over-interpreting the data, must be employed.</p>
</section>

<section class="research-projects">
  <h2>Projects</h2>

  <details class="project-item">
    <summary>Hierarchical mergers in GWTC-4</summary>
    <div class="project-body">
      <p class="project-authors">Plunkett, Callister, Zevin, Vitale &middot; <a href="https://journals.aps.org/prl/abstract/10.1103/n6p4-ftgq" target="_blank">Phys. Rev. Lett. 137, 021404 (2026)</a></p>
      <p><em>We find evidence for a hierarchical merger subpopulation in the GWTC-4 catalog.</em></p>
      <p>We can decompose binary black hole spins into the amount <em>aligned</em> with the orbit and the amount <em>perpendicular</em> to the orbit. Repeated black hole mergers populate a distinct shape in this plane. We analyze the population of black-hole mergers with a model that allows for a hierarchical-like component.</p>
      <p>We find strong evidence for complex structure in the spin distribution that is consistent with hierarchical formation. Moreover, this structure is mass-dependent. This suggests mechanisms that can produce highly spinning black holes operate at two distinct mass regimes.</p>
      <div class="project-figures">
        <figure class="project-figure">
          <img src="/assets/research/posterior-spline-ellipse-prior.png" alt="Inferred shape of the hierarchical-like component">
          <figcaption>The inferred shape of the hierarchical-like component.</figcaption>
        </figure>
        <figure class="project-figure">
          <img src="/assets/research/posterior-spline.png" alt="Fraction of highly-spinning black holes vs black hole mass">
          <figcaption>The fraction of highly-spinning (potentially hierarchical) black holes as a function of black hole mass.</figcaption>
        </figure>
      </div>
    </div>
  </details>

  <details class="project-item">
    <summary>Population III stars with next-generation detectors</summary>
    <div class="project-body">
      <p class="project-authors">Plunkett, Mould, Vitale &middot; <a href="https://journals.aps.org/prd/abstract/10.1103/jv8h-4ggy" target="_blank">Phys. Rev. D 112, 023039 (2025) </a></p>
      <p><em>We forecast the ability of future observatories like Einstein Telescope and Cosmic Explorer to constrain the demographics of Population III (metal-free) stellar populations.</em></p>
      <p>The first stars in the universe were critical for the chemical enrichment of future stellar generations, but their properties are poorly understood. Next-generation gravitational-wave detectors give us an opportunity to learn about Population III stars from the black holes they produce.</p>
      <p>We combine machine-learning with flexible data-driven methods to learn about the initial mass function and star formation history of Population III stars. With simulated observations in next-generation detectors, we show that we may be able to constrain these stellar properties from gravitational-waves.</p>
      <div class="project-figures">
        <figure class="project-figure">
          <img src="/assets/research/LOG_IMF_inference.png" alt="Inferred initial mass function of Population III stars">
          <figcaption>The inferred stellar initial mass function parameters for one of our simulated Population III cases.</figcaption>
        </figure>
        <figure class="project-figure">
          <img src="/assets/research/sfrd_inference.png" alt="Inferred star formation rate density of Population III stars">
          <figcaption>The inferred star formation rate for both of our simulated Population III cases.</figcaption>
        </figure>
      </div>
    </div>
  </details>

  <details class="project-item">
    <summary>Noise uncertainty in parameter estimation</summary>
    <div class="project-body">
      <p class="project-authors">Plunkett, Hourihane, Chatziioannou &middot; <a href="https://journals.aps.org/prd/abstract/10.1103/PhysRevD.106.104021" target="_blank">Phys. Rev. D 106, 104021 (2022)</a></p>
      <p><em>We investigated a method to concurrently estimate noise and compact-binary signal parameters in gravitational-wave data, reducing bias from mismodeled noise.</em></p>
      <p>Gravitational-wave data contains noise and, sometimes, a signal. When we model the signal parameters, we typically assume we know the noise exactly. However, in reality, we have uncertainty about the noise. We assess the impact of this assumption by contrasting the typical method with one that simultaneously fits for noise and signal parameters. We find that at O3 sensitivities, noise uncertainty has a subdominant effect.</p>
      <figure class="project-figure-single">
        <img src="/assets/research/150914_waveforms.png" alt="Comparison of inference methods for GW150914">
        <figcaption>Comparison of the two inference methods for GW150914, showing both time and frequency tracks. The two methods agree well, which we observe across the catalog.</figcaption>
      </figure>
    </div>
  </details>

</section>

<p class="research-cv-link">See my <a href="/cv/">CV</a> for a full list of publications and talks.</p>
