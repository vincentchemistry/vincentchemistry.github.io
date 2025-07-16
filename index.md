---
layout: default
title: Home
permalink: /
nav:
  order: 0
  tooltip: Go to homepage
---

# Welcome to the Liu Research Group

We design and study synthetic receptors for molecular recognition in water, with applications in health, energy, and environmental sustainability.

{% include section.html %}

## Highlights

{% capture text %}
Our group investigates synthetic receptors that operate in water using hydrogen bonding, electrostatic interactions, and other tunable noncovalent forces.

{%
  include button.html
  link="publications"
  text="See our publications"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}
{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="research"
  title="Our Research"
  text=text
%}

{% capture text %}
Explore our ongoing efforts to tackle challenges in sensing, separations, and catalysis through supramolecular chemistry.

{%
  include button.html
  link="projects"
  text="Browse our projects"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}
{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="projects"
  title="Our Projects"
  flip=true
  style="bare"
  text=text
%}

{% capture text %}
We are a vibrant team of students, postdocs, and collaborators based at USF Chemistry.

{%
  include button.html
  link="team"
  text="Meet our team"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}
{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="team"
  title="Our Team"
  text=text
%}
