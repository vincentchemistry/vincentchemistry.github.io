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

/* Grid view by default */
.media-container.grid-view .media-item {
  width: calc(33% - 20px);
  display: block;
}

/* List view styling */
.media-container.list-view {
  flex-direction: column;
}

.media-container.list-view .media-item {
  display: flex;
  flex-direction: row;
  gap: 20px;
  width: 100%;
}

.media-item {
  border: 1px solid #eee;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  display: none;
  background-color: #fff;
}

.media-item img,
.media-item video {
  width: 100%;
  border-radius: 8px;
}

/* List view media resizing */
.media-container.list-view .media-item img,
.media-container.list-view .media-item video {
  width: 300px;
  max-height: 200px;
  object-fit: cover;
}

.media-item h3 {
  margin-top: 10px;
  font-size: 16px;
}

.media-info {
  flex: 1;
  padding: 5px;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const topicFilter = document.getElementById("topicFilter");
  const mediaFilter = document.getElementById("mediaFilter");
  const layoutToggle = document.getElementById("layoutToggle");
  const container = document.querySelector(".media-container");
  const items = document.querySelectorAll(".media-item");

  // Default layout
  container.classList.add("grid-view");

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
    container.classList.toggle("grid-view");
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

<div class="media-container grid-view">

  <!-- GROUP PHOTOS -->
  <div class="media-item" data-topic="group" data-media="image">
    <img src="/assets/media/group_photo_2024.jpg" alt="Group Photo 2024">
    <div class="media-info">
      <h3>Group Photo – 2024</h3>
    </div>
  </div>

  <div class="media-item" data-topic="group" data-media="image">
    <img src="/assets/media/group_photo_2023.jpg" alt="Group Photo 2023">
    <div class="media-info">
      <h3>Group Photo – 2023</h3>
    </div>
  </div>

  <!-- JOURNAL COVERS -->
  <div class="media-item" data-topic="cover" data-media="image">
    <img src="/assets/media/JACS-2020.jpg" alt="XCAGE-Porp">
    <div class="media-info">
      <h3>Cover: XCage-Porp</h3>
    </div>
  </div>

  <div class="media-item" data-topic="cover" data-media="image">
    <img src="/assets/media/JACS-2021.jpg" alt="CD-Gold">
    <div class="media-info">
      <h3>Cover: CD-Gold</h3>
    </div>
  </div>

  <div class="media-item" data-topic="cover" data-media="image">
    <img src="/assets/media/JACS-2021-2.jpg" alt="glucose-pcage">
    <div class="media-info">
      <h3>Cover: glucose-pcage</h3>
    </div>
  </div>
  
  <div class="media-item" data-topic="cover" data-media="image">
    <img src="/assets/media/Chem-Sci-2024.png" alt="oxalate">
    <div class="media-info">
      <h3>Cover: oxalate</h3>
    </div>
  </div>
  
  <div class="media-item" data-topic="cover" data-media="image">
    <img src="/assets/media/Trends-Chem.jpg" alt="H-bond">
    <div class="media-info">
      <h3>Cover: H-bond</h3>
    </div>
  </div>
  
  <!-- RESEARCH VIDEOS -->
  <div class="media-item" data-topic="video" data-media="video">
    <video controls>
      <source src="/assets/media/foldamer-animation.mp4" type="video/mp4">
    </video>
    <div class="media-info">
      <h3>Foldamer Binding Mechanism</h3>
    </div>
  </div>

  <div class="media-item" data-topic="video" data-media="video">
    <video controls>
      <source src="/assets/media/cage-catalysis-demo.mp4" type="video/mp4">
    </video>
    <div class="media-info">
      <h3>Cage Catalysis in Water</h3>
    </div>
  </div>

</div>
