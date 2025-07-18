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
  width: 250px;
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

.publication-entry {
  margin-bottom: 60px;
  border-bottom: 1px solid #ccc;
  padding-bottom: 40px;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

.publication-citation {
  font-size: 16px;
  line-height: 1.8;
  font-family: "Georgia", serif;
  color: #222;
  max-width: 600px;
  margin: 0 auto;
}

.publication-image {
  display: block;
  margin: 20px auto;
  max-width: 600px;
  width: 100%;
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
  document.querySelectorAll('.publication-entry').forEach(entry => {
    entry.classList.remove('hidden');
    if (year !== 'all' && !entry.classList.contains('y' + year)) {
      entry.classList.add('hidden');
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

<!-- SEARCH + FILTER -->
<div class="search-filter-container">
  <div class="search-box">
    <input type="text" id="searchInput" placeholder="Search Publications" onkeyup="searchPublications()" />
  </div>
  <div class="filter-dropdown">
    <select id="yearFilter" onchange="filterPublicationsByYear()">
      <option value="all">All Years</option>
      <option value="2025">2025</option>
      <option value="2024">2024</option>
    </select>
  </div>
</div>

<!-- PUBLICATION LIST -->
{% assign pubs = site.data.publications %}
{% for pub in pubs %}
<div class="publication-entry y{{ pub.year }} {{ pub.topic }}">
  <div class="publication-citation">
    <strong>({{ forloop.index }})</strong> {{ pub.authors }} <em>{{ pub.title }}</em> <em>{{ pub.journal }}</em> <strong>{{ pub.year }}</strong>, <em>{{ pub.volume }}</em>, {{ pub.pages }}. <a href="{{ pub.link }}" target="_blank">[Link]</a>
  </div>
  <img class="publication-image" src="{{ pub.image }}" alt="TOC Graphic for {{ pub.title }}">
</div>
{% endfor %}
