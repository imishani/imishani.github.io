---
layout: page
permalink: /software/
title: software
description:
nav: true
nav_order: 4
---

## SRMP: Search-Based Robot Motion Planning

SRMP is a motion planning library for robot manipulators, built on graph search. It plans for a single arm or for teams of arms, runs inside the simulators and tools you already use, and was presented at IROS 2026. It is joint work with Yorai Shaoul and Ram Natarajan (equal contribution), Jiaoyang Li and Maxim Likhachev.

<p>
  <code>pip install srmp</code>
  &nbsp;
  <a href="https://srmp.readthedocs.io/en/latest/" class="btn btn-sm z-depth-0" role="button">Docs</a>
  <a href="https://arxiv.org/abs/2509.25352" class="btn btn-sm z-depth-0" role="button">Paper</a>
  <a href="https://discord.gg/3rnwRASfF" class="btn btn-sm z-depth-0" role="button">Discord</a>
</p>

### Why model-based planning still matters

- **High-stakes settings.** Robots working near people need guarantees, not likelihoods.
- **Hard problems.** Confined spaces and many arms sharing a workspace are hard to learn.
- **Robot learning.** Learned policies need many consistent, high-quality demonstrations, and a consistent planner can generate them.

### Consistent and predictable

Similar queries should get similar motions. SRMP uses search algorithms with theoretical guarantees, so a query that worked once will behave the same way next time. Sampling-based planners such as OMPL can return very different motions for nearly identical queries.

<figure class="srmp-video">
  <video src="{{ '/assets/video/srmp_consistency.mp4' | relative_url }}" poster="{{ '/assets/video/srmp_consistency.jpg' | relative_url }}" class="img-fluid rounded z-depth-1" autoplay muted loop playsinline preload="metadata"></video>
  <figcaption class="caption">SRMP vs. OMPL on similar queries: SRMP returns consistent motions.</figcaption>
</figure>

### Multi-arm planning

SRMP is the first motion planning library to support multi-arm manipulation planning directly, for teams of up to 10 arms.

<figure class="srmp-video">
  <video src="{{ '/assets/video/srmp_multi_arm.mp4' | relative_url }}" poster="{{ '/assets/video/srmp_multi_arm.jpg' | relative_url }}" class="img-fluid rounded z-depth-1" autoplay muted loop playsinline preload="metadata"></video>
  <figcaption class="caption">Multi-arm planning in simulation and on real robots.</figcaption>
</figure>

### Fast, and better plans

<div class="row text-center mt-3 mb-3">
  <div class="col-6 col-md-4 mb-3"><h3 class="mb-0">µs to ms</h3><small>planning time, single arm</small></div>
  <div class="col-6 col-md-4 mb-3"><h3 class="mb-0">ms to 2 s</h3><small>planning time, up to 10 arms</small></div>
  <div class="col-6 col-md-4 mb-3"><h3 class="mb-0">up to 2×</h3><small>higher success than sampling-based planners</small></div>
  <div class="col-6 col-md-6 mb-3"><h3 class="mb-0">10%</h3><small>of their solution cost</small></div>
  <div class="col-12 col-md-6 mb-3"><h3 class="mb-0">12.5%</h3><small>of their variation in cost</small></div>
</div>

### Agent mode

SRMP comes with a visual workspace where you build robot applications together with an AI agent. Describe the robots, scene and goal in plain language; the agent adds the robots and obstacles, picks a planner and solves the task; then you check the result in the visualizer and refine it yourself or through chat. It works with Gemini, Claude, GPT, Groq, or local models through Ollama.

<figure class="srmp-video">
  <video src="{{ '/assets/video/srmp_agent_mode.mp4' | relative_url }}" poster="{{ '/assets/video/srmp_agent_mode.jpg' | relative_url }}" class="img-fluid rounded z-depth-1" autoplay muted loop playsinline preload="metadata"></video>
  <figcaption class="caption">Asking the agent to build a small warehouse with arms and test their reachability.</figcaption>
</figure>

### A few lines of Python

If you prefer code, SRMP takes a few lines of Python and plugs into MuJoCo, PyBullet, Isaac and MoveIt!.

<figure class="srmp-video">
  <video src="{{ '/assets/video/srmp_python_api.mp4' | relative_url }}" poster="{{ '/assets/video/srmp_python_api.jpg' | relative_url }}" class="img-fluid rounded z-depth-1" autoplay muted loop playsinline preload="metadata"></video>
  <figcaption class="caption">Planning from Python and running the plan in a simulator and in MoveIt!.</figcaption>
</figure>

---

## Other Repositories

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
