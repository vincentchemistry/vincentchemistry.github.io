---
layout: default
title: Media
permalink: /media/
nav:
  order: 5
  tooltip: Group photos, covers, and videos
---

<style>
.media-filters {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  margin-bottom: 30px;
  align-items: center;
}

.media-filters select {
  padding: 10px;
  font-size: 14px;
  border-radius: 5px;
  border: 1px solid #ccc;
  background: white;
  cursor: pointer;
}

.media-section {
  margin-top: 60px;
}

.media-section h2 {
  font-size: 24px;
  border-bottom: 2px solid #eee;
  padding-bottom: 10px;
  margin-bottom: 30px;
}

.media-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.media-item {
  width: calc(33% - 20px);
  border: 1px solid #eee;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  background-color: #fff;
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

<script>
document.addEventListener("DOMContentLoaded", function () {
  const topicFilter = document.getElementById("topicFilter");
  const mediaFilter = document.getElementById("mediaFilter");
  const items = document.querySelectorAll(".media-item");

  function filterMedia() {
    const selectedTopic = topicFilter.value;
    const selectedMedia = mediaFilter.value;

    items.forEach(item => {
      const matchesTopic = (selectedTopic === "all" || item.dataset.topic === selectedTopic);
      const matchesMedia = (selectedMedia === "all" || item.dataset.media === selectedMedia);
      item.style.display = matchesTopic && matchesMedia ? "block" : "none";
    });
  }

  topicFilter.addEventListener("change", filterMedia);
  mediaFilter.addEventListener("change", filterMedia);
});
</script>

<h1>Media</h1>

<div class="media-filters">
  <label>Topic:
    <select id="topicFilter">
      <option value="all">All Topics</option>
      <option value="group">Group Photos</option>
      <option value="cover">Journal Covers</option>
      <option value="video">Research Videos</option>
    </select>
  </label>

  <label>Media Type:
    <select id="mediaFilter">
      <option value="all">All Media</option>
      <option value="image">Images</option>
      <option value="video">Videos</option>
    </select>
  </label>
</div>

<!-- GROUP PHOTOS -->
<div class="media-section">
  <h2>Group Photos</h2>
  <div class="media-grid">
    <div class="media-item" data-topic="group" data-media="image">
      <a href="/assets/media/group_photo_2024.jpg" data-lightbox="group" data-title="Group Photo – 2024">
        <img src="/assets/media/group_photo_2024.jpg" alt="Group Photo – 2024" loading="lazy">
      </a>
      <h3>Group Photo – 2024</h3>
    </div>
    <div class="media-item" data-topic="group" data-media="image">
      <a href="/assets/media/group_photo_2023.jpg" data-lightbox="group" data-title="Group Photo – 2023">
        <img src="/assets/media/group_photo_2023.jpg" alt="Group Photo – 2023" loading="lazy">
      </a>
      <h3>Group Photo – 2023</h3>
    </div>
  </div>
</div>

<!-- JOURNAL COVERS -->
<div class="media-section">
  <h2>Journal Covers</h2>
  <div class="media-grid">
    <div class="media-item" data-topic="cover" data-media="image">
      <a href="/assets/media/JACS-2020.jpg" data-lightbox="cover" data-title="Cover: XCage-Porp">
        <img src="/assets/media/JACS-2020.jpg" alt="XCage-Porp" loading="lazy">
      </a>
      <h3>Cover: XCage-Porp</h3>
    </div>
    <div class="media-item" data-topic="cover" data-media="image">
      <a href="/assets/media/JACS-2021.jpg" data-lightbox="cover" data-title="Cover: CD-Gold">
        <img src="/assets/media/JACS-2021.jpg" alt="CD-Gold" loading="lazy">
      </a>
      <h3>Cover: CD-Gold</h3>
    </div>
    <div class="media-item" data-topic="cover" data-media="image">
      <a href="/assets/media/JACS-2021-2.jpg" data-lightbox="cover" data-title="Cover: Glucose-pCage">
        <img src="/assets/media/JACS-2021-2.jpg" alt="Glucose-pCage" loading="lazy">
      </a>
      <h3>Cover: Glucose-pCage</h3>
    </div>
    <div class="media-item" data-topic="cover" data-media="image">
      <a href="/assets/media/Chem-Sci-2024.png" data-lightbox="cover" data-title="Cover: Oxalate">
        <img src="/assets/media/Chem-Sci-2024.png" alt="Oxalate" loading="lazy">
      </a>
      <h3>Cover: Oxalate</h3>
    </div>
    <div class="media-item" data-topic="cover" data-media="image">
      <a href="/assets/media/Trends-Chem.jpg" data-lightbox="cover" data-title="Cover: H-bond">
        <img src="/assets/media/Trends-Chem.jpg" alt="H-bond" loading="lazy">
      </a>
      <h3>Cover: H-bond</h3>
    </div>
  </div>
</div>

<!-- RESEARCH VIDEOS -->
<div class="media-section">
  <h2>Research Videos</h2>
  <div class="media-grid">
    <div class="media-item" data-topic="video" data-media="video">
      <video controls loading="lazy">
        <source src="/assets/media/foldamer-animation.mp4" type="video/mp4">
      </video>
      <h3>Foldamer Binding Mechanism</h3>
    </div>
    <div class="media-item" data-topic="video" data-media="video">
      <video controls loading="lazy">
        <source src="/assets/media/cage-catalysis-demo.mp4" type="video/mp4">
      </video>
      <h3>Cage Catalysis in Water</h3>
    </div>
  </div>
</div>
