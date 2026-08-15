---
layout: about
title: about
permalink: /
subtitle: <a href='https://www.ri.cmu.edu/robotics-groups/search-based-planning-laboratory/'>Search-based Planning Lab (SBPL)</a>. <a href='https://www.ri.cmu.edu'>Robotics Institute</a>. <a href='https://www.cmu.edu'>Carnegie Mellon University</a>.

profile:
  align: right
  image: profile_me.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p> 1612E Newell-Simon Hall </p>
    <p> 5000 Forbes Ave </p>
    <p> Pittsburgh, PA 15213 </p>

news: true # includes a list of news items
latest_posts: false # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

I am a PhD Student at <a href='https://www.ri.cmu.edu'>The Robotics Institute</a>, Carnegie Mellon University, advised by <a href='https://www.cs.cmu.edu/~maxim/'>Maxim Likhachev</a>.
I build planning algorithms that let robots act reliably in the real world — and I care as much about the guarantees they come with as about the tasks they solve.

Most of my work is on search, and how far it can be pushed. In long-horizon manipulation, I treat skills as active participants in the search rather than fixed primitives, using physics simulation to judge where they are likely to succeed (<a href='https://skill-mosaic.github.io/'>MOSAIC</a>).
In multi-robot settings, I work on planning concurrent motions for teams of arms in cluttered, obstacle-laden workspaces (<a href='https://x-cbs.github.io'>xECBS</a>, <a href='https://multi-robot-diffusion.github.io/'>MMD</a>).
And in high-dimensional spaces, I am interested in the observation that a single search graph is rarely the right structure to begin with (<a href='https://multi-graph-search.github.io/'>MGS</a>).

A thread running through all of it is combining learned models with search — using diffusion models and actor-critic networks to generate and guide, while keeping the completeness and bounded-suboptimality guarantees that search gives you.
Much of this work is released in <a href='https://srmp.readthedocs.io/'>SRMP</a>, a search-based motion planning library for single- and multi-robot manipulation, with Python and C++ APIs, support for MuJoCo, PyBullet, Isaac and Genesis, and a MoveIt! plugin for deployment on hardware.

Previously, I was a Master's Student at <a href='https://english.tau.ac.il/'>Tel Aviv University</a>, advised by <a href='http://web2.eng.tau.ac.il/wtest/Avishailab/index.php/sintov/'>Avishai Sintov</a> at <a href='http://web2.eng.tau.ac.il/wtest/Avishailab/'>TAU Robotics Lab</a>, where I worked on dual-arm manipulation of elastic wires using only force/torque feedback.
