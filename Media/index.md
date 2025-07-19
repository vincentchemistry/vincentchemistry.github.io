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
}

.media-filters select,
.media-filters button {
  padding: 10px;
  font-size: 14px;
  border-radius: 5px;
  border: 1px solid #ccc;
  background: white;
  cursor: pointer;
}

.media-container {
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
  display: none;
}

.media-item img, .media-item video {
  width: 100%;
  border-radius: 8px;
}

.media-item h3 {
  margin-top: 10px;
  font-size: 16px;
}

.layout-toggle {
  margin-left: auto;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const topicFilter = document.getElementById("topicFilter");
  const mediaFilter = document.getElementById("mediaFilter");
  const layoutToggle = document.getElementById("layoutToggle");
  const items = document.querySelectorAll(".media-item");

  function filterMedia() {
    const topic = topicFilter.value;
    const media = mediaFilter.value;

    items.forEach(item => {
      const matchesTopic = (topic === "all" || item.dataset.topic === topic);
      const matchesMedia = (media === "all" || item.dataset.media === media);
      item.style.display = matchesTopic && matchesMedia ? "block" : "none";
    });
  }

  function toggleLayout() {
    const container = document.querySelector(".media-container");
    container.classList.toggle("list-view");
  }

  topicFilter.addEventListener("change", filterMedia);
  mediaFilter.addEventListener("change", filterMedia);
  layoutToggle.addEventListener("click", toggleLayout);
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

  <button id="layoutToggle" class="layout-toggle">Toggle Layout</button>
</div>

<div class="media-container">

  <!-- GROUP PHOTOS -->
  <div class="media-item" data-topic="group" data-media="image">
    <img src="/assets/media/group_photo_2024.jpg" alt="Group Photo 2024">
    <h3>Group Photo – 2024</h3>
  </div>

  <div class="media-item" data-topic="group" data-media="image">
    <img src="/assets/media/group_photo_2023.jpg" alt="Group Photo 2023">
    <h3>Group Photo – 2023</h3>
  </div>

  <!-- JOURNAL COVERS -->
  <div class="media-item" data-topic="cover" data-media="image">
    <img src="/assets/media/cover_macrocycle.jpg" alt="Macrocycle Cover">
    <h3>Cover: Pyridinium Macrocycle</h3>
  </div>

  <div class="media-item" data-topic="cover" data-media="image">
    <img src="/assets/media/cover_cage.jpg" alt="Cationic Cage Cover">
    <h3>Cover: Tricationic Hydrogen Bonding Cage</h3>
  </div>

  <!-- RESEARCH VIDEOS -->
  <div class="media-item" data-topic="video" data-media="video">
    <video controls>
      <source src="/assets/media/foldamer-animation.mp4" type="video/mp4">
    </video>
    <h3>Foldamer Binding Mechanism</h3>
  </div>

  <div class="media-item" data-topic="video" data-media="video">
    <video controls>
      <source src="/assets/media/cage-catalysis-demo.mp4" type="video/mp4">
    </video>
    <h3>Cage Catalysis in Water</h3>
  </div>

</div>

