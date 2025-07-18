---
layout: default
title: Publications
permalink: /publications/
nav:
  order: 6
  tooltip: View our publications
---
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

.search-box button {
  background-color: #5A2A82;
  border: none;
  padding: 10px 14px;
  border-radius: 5px;
  cursor: pointer;
}

.search-box button svg {
  fill: white;
  width: 16px;
  height: 16px;
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

.hidden {
  display: none;
}
</style>

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

<!-- Example Publication -->
<div class="publication-entry y2025 anion">
  <div class="publication-citation">
    <strong>(48)</strong> Zhou, P.; Cheng, K.; Qu, K.; Wang, L.; Hu, C.; <strong>Liu, W.</strong>; Chen, H. <em>An electric molecular Faraday cage.</em> <em>J. Am. Chem. Soc.</em> <strong>2025</strong>, <em>147</em>, 19272–19281. <a href="https://doi.org/10.1021/jacs.5c01234" target="_blank">[Link]</a>
  </div>
  <img class="publication-image" src="/assets/images/publications/zhou2025jacs.png" alt="TOC Graphic for Zhou et al. JACS 2025">
</div>

<div class="publication-entry y2024 carbohydrate">
  <div class="publication-citation">
    <strong>(47)</strong> Liu, W.; Tan, L.; Chen, M. <em>Pyridinium-bridged macrocycles for glucose binding in water.</em> <em>Chem. Sci.</em> <strong>2024</strong>, <em>15</em>, 4567–4578. <a href="https://doi.org/10.1039/d4sc04567a" target="_blank">[Link]</a>
  </div>
  <img class="publication-image" src="/assets/images/publications/liu2024chemsci.png" alt="TOC Graphic for Liu et al. Chem Sci 2024">
</div>

