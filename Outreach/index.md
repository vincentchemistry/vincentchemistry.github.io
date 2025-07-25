---
layout: default
title: Outreach
permalink: /outreach/
nav:
  order: 7
  tooltip: Education and outreach
---

<!-- STYLES -->
<style>
.media-section {
  margin-top: 40px;
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
}

.media-header {
  font-size: 20px;
  font-weight: bold;
  background-color: #f7f7f7;
  padding: 15px 20px;
  cursor: pointer;
  border-bottom: 1px solid #ddd;
}

.media-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  padding: 20px;
  justify-content: center;
}

.media-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  flex: 1 1 calc(33.333% - 20px);
  max-width: calc(33.333% - 20px);
  border: 1px solid #eee;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  background-color: #fff;
  text-align: center;
}

@media (max-width: 768px) {
  .media-item {
    flex: 1 1 calc(50% - 20px);
    max-width: calc(50% - 20px);
  }
}

@media (max-width: 480px) {
  .media-item {
    flex: 1 1 100%;
    max-width: 100%;
  }
}

.media-item img,
.media-item video {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
  display: block;
  margin: 0 auto;
}

.media-item h3 {
  margin-top: 10px;
  font-size: 16px;
}
</style>

<!-- LIGHTBOX2 SUPPORT -->
<link href="https://cdn.jsdelivr.net/npm/lightbox2@2/dist/css/lightbox.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/lightbox2@2/dist/js/lightbox-plus-jquery.min.js"></script>

<!-- TOGGLE SCRIPT -->
<script>
document.addEventListener("DOMContentLoaded", function () {
  const headers = document.querySelectorAll(".media-header");
  headers.forEach(header => {
    header.addEventListener("click", function () {
      const content = this.nextElementSibling;
      content.style.display = content.style.display === "none" ? "flex" : "none";
    });
  });
});
</script>

<h1>Outreach Activities</h1>

<!-- 2025 -->
<div class="media-section">
  <div class="media-header">2025: Outreach Highlights</div>
  <div class="media-grid">
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group-2025" data-title="USF Outward Bound - Zoo Tampa">
        <img src="/assets/media/12.14.2024.png" alt="USF Outward Bound at Zoo Tampa" loading="lazy">
      </a>
      <h3>USF Outward Bound</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/09.12.2024.png" data-lightbox="group-2025" data-title="St. Pete Science Festival - Bowlero Night">
        <img src="/assets/media/09.12.2024.png" alt="St. Pete Science Festival" loading="lazy">
      </a>
      <h3>St. Pete Science Festival</h3>
    </div>
  </div>
</div>

<!-- 2024 -->
<div class="media-section">
  <div class="media-header">2024: Outreach Events</div>
  <div class="media-grid">
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group-2024" data-title="USF Outward Bound - Zoo Tampa">
        <img src="/assets/media/12.14.2024.png" alt="USF Outward Bound at Zoo Tampa" loading="lazy">
      </a>
      <h3>USF Outward Bound</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/09.12.2024.png" data-lightbox="group-2024" data-title="Dunedin Middle School Visit">
        <img src="/assets/media/09.12.2024.png" alt="Dunedin Middle School" loading="lazy">
      </a>
      <h3>Dunedin Middle School</h3>
    </div>
  </div>
</div>

<!-- 2023 -->
<div class="media-section">
  <div class="media-header">2023: Middle School Engagements</div>
  <div class="media-grid">
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group-2023" data-title="Seminole Middle School">
        <img src="/assets/media/12.14.2024.png" alt="Seminole Middle School" loading="lazy">
      </a>
      <h3>Seminole Middle School</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/09.12.2024.png" data-lightbox="group-2023" data-title="Oak Grove Middle School">
        <img src="/assets/media/09.12.2024.png" alt="Oak Grove Middle School" loading="lazy">
      </a>
      <h3>Oak Grove Middle School</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group-2023" data-title="USF Upward Bound">
        <img src="/assets/media/12.14.2024.png" alt="USF Upward Bound" loading="lazy">
      </a>
      <h3>USF Upward Bound</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group-2023" data-title="Thurgood Marshall Middle School">
        <img src="/assets/media/12.14.2024.png" alt="Thurgood Marshall Middle School" loading="lazy">
      </a>
      <h3>Thurgood Marshall Middle School</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group-2023" data-title="Morgan Fitzgerald Middle School">
        <img src="/assets/media/12.14.2024.png" alt="Morgan Fitzgerald Middle School" loading="lazy">
      </a>
      <h3>Morgan Fitzgerald Middle School</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group-2023" data-title="Tyrone Middle School">
        <img src="/assets/media/12.14.2024.png" alt="Tyrone Middle School" loading="lazy">
      </a>
      <h3>Tyrone Middle School</h3>
    </div>
  </div>
</div>
