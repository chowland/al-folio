---
layout: page
permalink: /repositories/
title: repositories
description: An overview of the software I work on, and some of my favourite open-source projects by other people
nav: true
nav_order: 3
---

**Watch this space!**
I am working on an open-source release for my current simulation code.
`AFiD-MuRPhFi` is a sizeable extension to the second-order finite difference solver [`AFiD`](https://github.com/PhysicsOfFluids/AFiD), which includes

- a multiple-resolution method, allowing for the solution of a slowly diffusing scalar on a higher resolution grid than the velocity
- implementation of the phase-field method of [Hester et al. (2020)](https://doi.org/) to simulate melting objects, making use of the multiple-resolution method to simulate the diffuse liquid-solid interface at a higher resolution

`MuRPhFi` is an acronym for 'Multiple Resolution Phase-Field'.
If you would like early access to the code, just let me know by [sending me an email](mailto:c.j.howland@utwente.nl).
And if you're just curious, then please check out the (in progress) [documentation](https://chowland.github.io/AFiD-MuRPhFi).

## GitHub users

{% if site.data.repositories.github_users %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
  {% if site.data.repositories.github_users.size > 1 %}
  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.html username=user %}
  </div>

  ---

{% endfor %}
{% endif %}
{% endif %}

## GitHub Repositories
<div class="projects">
<h2 class="category">my repos</h2>
{% if site.data.repositories.my_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.my_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

<h2 class="category">my favourites</h2>
{% if site.data.repositories.fav_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.fav_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
</div>
{% endif %}