---
layout: default
title: Media
permalink: /media/
nav:
  order: 5
  tooltip: Group photos, covers, and videos
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
}

.media-item {
  flex: 1 1 calc(33.333% - 20px);
  max-width: calc(33.333% - 20px);
  border: 1px solid #eee;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  background-color: #fff;
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
  width: 100%;
  border-radius: 8px;
  height: auto;
  display: block;
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

<h1>Media</h1>

<!-- GROUP PHOTOS -->
<div class="media-section">
  <div class="media-header">Group Photos</div>
  <div class="media-grid">
    <div class="media-item">
      <a href="/assets/media/12.14.2024.png" data-lightbox="group" data-title="2024 Zoo Tampa">
        <img src="/assets/media/12.14.2024.png" alt="2024 Zoo Tampa" loading="lazy">
      </a>
      <h3>2024 Zoo Tampa</h3>
      </div>
    <div class="media-item">
      <a href="/assets/media/09.12.2024.png" data-lightbox="group" data-title="2024 bowling night at Bowlero">
        <img src="/assets/media/09.12.2024.png" alt="2024 bowling night at Bowlero" loading="lazy">
      </a>
      <h3>2024 bowling night at Bowlero</h3>
       </div>
    <div class="media-item">
      <a href="/assets/media/03.30.2024.png" data-lightbox="group" data-title="2024 Lettuce Lake Park">
        <img src="/assets/media/03.30.2024.png" alt="2024 Lettuce Lake Park" loading="lazy">
      </a>
      <h3>2024 Lettuce Lake Park</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/12.15.2023.png" data-lightbox="group" data-title="2023 Weeki Wachee Spring State Park">
        <img src="/assets/media/12.15.2023.png" alt="2023 Weeki Wachee Spring State Park" loading="lazy">
      </a>
      <h3>2023 Weeki Wachee Spring State Park</h3>
       </div>
    <div class="media-item">
      <a href="/assets/media/06.15.2023.png" data-lightbox="group" data-title="2023 First Group Photo">
        <img src="/assets/media06.15.2023.png" alt="2023 First Group Photo" loading="lazy">
      </a>
      <h3>2023 First Group Photo</h3>
    </div>
  </div>
</div>

<!-- JOURNAL COVERS -->
<div class="media-section">
  <div class="media-header">Journal Covers</div>
  <div class="media-grid">
    <div class="media-item">
      <a href="/assets/media/Trends-Chem.jpg" data-lightbox="cover" data-title="Cover: H-bond">
        <img src="/assets/media/Trends-Chem.jpg" alt="H-bond" loading="lazy">
      </a>
      <h3>Cover: Trends-Chem-2025</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/Chem-Sci-2024.png" data-lightbox="cover" data-title="Cover: Oxalate">
        <img src="/assets/media/Chem-Sci-2024.png" alt="Oxalate" loading="lazy">
      </a>
      <h3>Cover: Chem-Sci-2024</h3>
    </div>
       <div class="media-item">
      <a href="/assets/media/JACS-2021-2.jpg" data-lightbox="cover" data-title="Cover: Glucose-pCage">
        <img src="/assets/media/JACS-2021-2.jpg" alt="Glucose-pCage" loading="lazy">
      </a>
      <h3>Cover: JACS-2021-2</h3>
    </div>
        <div class="media-item">
      <a href="/assets/media/JACS-2021.jpg" data-lightbox="cover" data-title="Cover: CD-Gold">
        <img src="/assets/media/JACS-2021.jpg" alt="CD-Gold" loading="lazy">
      </a>
      <h3>Cover: JACS-2021</h3>
    </div>
    <div class="media-item">
      <a href="/assets/media/JACS-2020.jpg" data-lightbox="cover" data-title="Cover: XCage-Porp">
        <img src="/assets/media/JACS-2020.jpg" alt="XCage-Porp" loading="lazy">
      </a>
      <h3>Cover: JACS-2020</h3>
    </div>
  </div>
</div>

<!-- RESEARCH VIDEOS -->
<div class="media-section">
  <div class="media-header">Research Videos</div>
  <div class="media-grid">
    <div class="media-item">
      <video controls loading="lazy">
        <source src="/assets/media/foldamer-animation.mp4" type="video/mp4">
      </video>
      <h3>Foldamer Binding Mechanism</h3>
    </div>
    <div class="media-item">
      <video controls loading="lazy">
        <source src="/assets/media/cage-catalysis-demo.mp4" type="video/mp4">
      </video>
      <h3>Cage Catalysis in Water</h3>
    </div>
  </div>
</div>
