---
layout: page
permalink: /software/
title: software
description:
nav: true
nav_order: 4
---

## SRMP: Search-Based Robot Motion Planning

<div class="row">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/srmp_gif.webp" title="SRMP" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    <p>SRMP is a search-based motion planning library for single- and multi-robot manipulation, presented at IROS 2026. It works with MuJoCo, PyBullet, Isaac and other simulators, has Python and C++ APIs, and includes a MoveIt! plugin for running plans on real robots.</p>
    <p><code>pip install srmp</code></p>
    <p>
      <a href="https://srmp.readthedocs.io/en/latest/" class="btn btn-sm z-depth-0" role="button">Docs</a>
      <a href="https://arxiv.org/abs/2509.25352" class="btn btn-sm z-depth-0" role="button">Paper</a>
      <a href="https://discord.gg/3rnwRASfF" class="btn btn-sm z-depth-0" role="button">Discord</a>
    </p>
  </div>
</div>

---

## Other Repositories

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
