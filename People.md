---
layout: default
title: Our Team
permalink: /people/
---

<style>
.people-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
  gap: 2rem;
  justify-items: center;
  margin-top: 2rem;
}

.person {
  text-align: center;
  max-width: 180px;
}

.person img {
  width: 150px;
  height: 150px;
  object-fit: cover;
  border-radius: 50%;
  margin-bottom: 0.5rem;
}
</style>

# Our Team

---

## Principal Investigator

<div class="people-grid">
{% assign pi = site.data.members | where: "role", "Principal Investigator" %}
{% for person in pi %}
<div class="person">
  <img src="/{{ person.image }}" alt="{{ person.name }}">
  <strong>{{ person.name }}</strong><br/>
  {{ person.role }}<br/>
  <a href="mailto:{{ person.email }}">{{ person.email }}</a>
</div>
{% endfor %}
</div>

---

## Graduate Students

<div class="people-grid">
{% assign grads = site.data.members | where: "role", "Graduate Student" %}
{% for person in grads %}
<div class="person">
  <img src="/{{ person.image }}" alt="{{ person.name }}">
  <strong>{{ person.name }}</strong><br/>
  {{ person.role }}<br/>
  <a href="mailto:{{ person.email }}">{{ person.email }}</a>
</div>
{% endfor %}
</div>

---

## Undergraduate Students

<div class="people-grid">
{% assign undergrads = site.data.members | where: "role", "Undergraduate Student" %}
{% for person in undergrads %}
<div class="person">
  <img src="/{{ person.image }}" alt="{{ person.name }}">
  <strong>{{ person.name }}</strong><br/>
  {{ person.role }}<br/>
  <a href="mailto:{{ person.email }}">{{ person.email }}</a>
</div>
{% endfor %}
</div>

---

## Alumni

<div class="people-grid">
{% assign alumni = site.data.members | where: "role", "Alumni" %}
{% for person in alumni %}
<div class="person">
  <img src="/{{ person.image }}" alt="{{ person.name }}">
  <strong>{{ person.name }}</strong><br/>
  {{ person.role }}<br/>
</div>
{% endfor %}
</div>
