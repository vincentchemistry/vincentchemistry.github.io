---
layout: default
title: Members
permalink: /team/
nav:
  order: 4
  tooltip: Meet the team
---
---
layout: people
title: Members
permalink: /members/
---

# Group Members

<div class="people-grid">

<!-- Principal Investigator -->
<div class="person-card">
  <img src="{{ '/assets/images/members/liu.jpg' | relative_url }}" alt="Dr. Wenqi Liu" />
  <h2>Dr. Wenqi Liu</h2>
  <p class="position">Principal Investigator</p>
  <p>Assistant Professor of Chemistry, University of South Florida</p>
  <p><a href="{{ '/members#Wenqi-Liu' | relative_url }}">[Profile]</a></p>
</div>

<!-- Postdoctoral Fellow -->
<div class="person-card">
  <img src="{{ '/assets/images/members/zhai.jpg' | relative_url }}" alt="Dr. Canjia Zhai" />
  <h2>Dr. Canjia Zhai</h2>
  <p class="position">Postdoctoral Fellow</p>
  <p>B.S./M.S. Peking University; Ph.D. University of Notre Dame</p>
</div>

<!-- Graduate Students -->
{% assign grad = site.members | where:"role","Graduate Student" %}
{% for person in grad %}
<div class="person-card">
  <img src="{{ '/assets/images/members/' | append: person.image | relative_url }}" alt="{{ person.name }}" />
  <h2>{{ person.name }}</h2>
  <p class="position">Graduate Student</p>
  <p>{{ person.bio }}</p>
  <p><a href="mailto:{{ person.email }}">[Email]</a></p>
</div>
{% endfor %}

<!-- Undergraduate Students -->
{% assign undergrad = site.members | where:"role","Undergraduate Student" %}
{% for person in undergrad %}
<div class="person-card">
  <img src="{{ '/assets/images/members/' | append: person.image | relative_url }}" alt="{{ person.name }}" />
  <h2>{{ person.name }}</h2>
  <p class="position">Undergraduate Researcher</p>
  <p>{{ person.bio }}</p>
</div>
{% endfor %}

</div>

