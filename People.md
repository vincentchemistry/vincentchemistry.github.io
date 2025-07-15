---
layout: default
title: Our Team
permalink: /people/
---

## Principal Investigator

{% assign pi = site.data.members | where: "role", "Principal Investigator" %}
{% for person in pi %}
### {{ person.name }}
![Photo of {{ person.name }}]({{ person.image }}){: width="150px" style="float: left; margin-right: 20px;"}
{{ person.bio }}

[Website]({{ person.website }}) • [Email](mailto:{{ person.email }})
{% endfor %}

<br clear="all" />

## Graduate Students

{% assign grads = site.data.members | where: "role", "Graduate Student" %}
{% for person in grads %}
### {{ person.name }}
![Photo of {{ person.name }}]({{ person.image }}){: width="150px" style="float: left; margin-right: 20px;"}
{{ person.bio }}

[Email](mailto:{{ person.email }})
{% endfor %}

<br clear="all" />

## Undergraduate Students

{% assign undergrads = site.data.members | where: "role", "Undergraduate Student" %}
{% for person in undergrads %}
### {{ person.name }}
![Photo of {{ person.name }}]({{ person.image }}){: width="150px" style="float: left; margin-right: 20px;"}
{{ person.bio }}

[Email](mailto:{{ person.email }})
{% endfor %}
