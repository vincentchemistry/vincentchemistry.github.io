---
layout: default
title: Publications
permalink: /publications/
nav:
  order: 5
  tooltip: Group publications
---

<!-- STYLES -->
<style>
.publication-container {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 20px;
}

.search-filter-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 30px;
  gap: 10px;
}

.search-box input {
  padding: 10px;
  width: 100%;
  max-width: 250px;
  font-size: 14px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.filter-dropdown select {
  padding: 10px;
  font-size: 14px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.year-group {
  margin-top: 60px;
}

.year-group h2 {
  border-bottom: 2px solid #ccc;
  padding-bottom: 5px;
  font-size: 24px;
  color: #333;
}

.publication-entry {
  margin-bottom: 60px;
  padding-bottom: 40px;
  border-bottom: 1px solid #ddd;
}

.publication-citation {
  font-size: 16px;
  line-height: 1.8;
  font-family: "Georgia", serif;
  color: #222;
}

.publication-image {
  display: block;
  margin: 20px auto;
  width: 66%;
  max-width: 640px;
  height: auto;
  border: 1px solid #ddd;
  border-radius: 6px;
  box-shadow: 2px 2px 6px rgba(0,0,0,0.1);
}

.hidden {
  display: none;
}
</style>

<!-- JAVASCRIPT -->
<script>
function filterPublicationsByYear() {
  let year = document.getElementById('yearFilter').value;
  document.querySelectorAll('.year-group').forEach(group => {
    if (year === 'all' || group.dataset.year === year) {
      group.classList.remove('hidden');
    } else {
      group.classList.add('hidden');
    }
  });
}

function searchPublications() {
  let input = document.getElementById('searchInput').value.toLowerCase();
  document.querySelectorAll('.publication-entry').forEach(entry => {
    const text = entry.textContent.toLowerCase();
    if (text.includes(input)) {
      entry.classList.remove('hidden');
    } else {
      entry.classList.add('hidden');
    }
  });
}
</script>

# Publications

<div class="publication-container">

  <!-- SEARCH + FILTER -->
  <div class="search-filter-container">
    <div class="search-box">
      <input type="text" id="searchInput" placeholder="Search Publications" onkeyup="searchPublications()" />
    </div>
    <div class="filter-dropdown">
      <select id="yearFilter" onchange="filterPublicationsByYear()">
        <option value="all">All Years</option>
        {% assign years = site.data.publications | map: "year" | uniq | sort | reverse %}
        {% for year in years %}
        <option value="{{ year }}">{{ year }}</option>
        {% endfor %}
      </select>
    </div>
  </div>

  <!-- PUBLICATIONS GROUPED BY YEAR -->
  {% assign pubs = site.data.publications %}
  {% assign total = pubs.size %}
  {% assign current_year = nil %}
  {% assign count = 0 %}

  {% for pub in pubs %}
    {% unless pub.year == current_year %}
      {% if forloop.index > 1 %}
        </div> <!-- Close previous year-group -->
      {% endif %}
      <div class="year-group" data-year="{{ pub.year }}">
        <h2>{{ pub.year }}</h2>
      {% assign current_year = pub.year %}
    {% endunless %}

    {% assign number = total | minus: count %}
    <div class="publication-entry y{{ pub.year }} {{ pub.topic }}">
      <div class="publication-citation">
        <strong>({{ number }})</strong>
        {{ pub.authors }} <em>{{ pub.title }}</em>
        <em>{{ pub.journal }}</em> <strong>{{ pub.year }}</strong>,
        <em>{{ pub.volume }}</em>, {{ pub.pages }}.
        <a href="{{ pub.link }}" target="_blank">[Link]</a>
      </div>
      <img class="publication-image" src="{{ pub.image }}" alt="TOC Graphic for {{ pub.title }}">
    </div>
    {% assign count = count | plus: 1 %}
  {% endfor %}
  </div> <!-- Close last year-group -->

</div>
