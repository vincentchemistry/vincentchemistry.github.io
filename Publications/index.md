---
layout: default
title: Publications
permalink: /publications/
nav:
  order: 6
  tooltip: View our publications
---

<style>
.filter-buttons {
  margin-bottom: 30px;
}
.filter-buttons button {
  background: #f0f0f0;
  border: none;
  padding: 10px 16px;
  margin: 5px;
  border-radius: 20px;
  cursor: pointer;
  font-weight: bold;
}
.filter-buttons button.active {
  background: #007ACC;
  color: white;
}

.publication-entry {
  margin-bottom: 60px;
  border-bottom: 1px solid #ccc;
  padding-bottom: 40px;
}

.publication-citation {
  font-size: 16px;
  line-height: 1.8;
  font-family: "Georgia", serif;
  color: #222;
}

.publication-image {
  max-width: 100%;
  height: auto;
  margin: 20px 0;
  border: 1px solid #ddd;
  border-radius: 6px;
  box-shadow: 2px 2px 6px rgba(0,0,0,0.1);
}
</style>

<script>
function filterPublications(category) {
  let entries = document.querySelectorAll('.publication-entry');
  entries.forEach(entry => {
    if (category === 'all' || entry.classList.contains(category)) {
      entry.classList.remove('hidden');
    } else {
      entry.classList.add('hidden');
    }
  });

  document.querySelectorAll('.filter-buttons button').forEach(btn => btn.classList.remove('active'));
  document.getElementById('btn-' + category).classList.add('active');
}
</script>

Warning! Copyrights to the publications are held by their publishers. The copies provided here are only for personal use and may not be reposted on other websites or used for any other purpose without the permission of publishers.

# Publications

<div class="filter-buttons">
  <button id="btn-all" class="active" onclick="filterPublications('all')">All</button>
  <button id="btn-2025" onclick="filterPublications('y2025')">2025</button>
  <button id="btn-2024" onclick="filterPublications('y2024')">2024</button>
  <button id="btn-anion" onclick="filterPublications('anion')">Anion Binding</button>
  <button id="btn-carbohydrate" onclick="filterPublications('carbohydrate')">Carbohydrate Recognition</button>
</div>

<!-- Example Publication -->
<div class="publication-entry y2025 anion">
  <div class="publication-citation">
    <strong>(48)</strong> Zhou, P.; Cheng, K.; Qu, K.; Wang, L.; Hu, C.; <strong>Liu, W.</strong>; Chen, H. <em>An electric molecular Faraday cage.</em> <em>J. Am. Chem. Soc.</em> <strong>2025</strong>, <em>147</em>, 19272–19281. <a href="https://doi.org/10.1021/jacs.5c01234" target="_blank">[Link]</a>
  </div>
  <img class="publication-image" src="/assets/images/publications/zhou2025jacs.png" alt="TOC Graphic for Zhou et al. JACS 2025">
</div>
