---
layout: page
permalink: /cdi-lab/
title: CDI lab LV group
description: Living with Vision Group @ CDI Lab
nav: true
nav_order: 3
---

<!-- Swiper Carousel for WDCC2025 -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11.0.5/swiper-bundle.min.css">
<style>
  .swiper-container {
    width: 100%;
    height: 500px;
    margin-bottom: 40px;
  }
  .swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .swiper-slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .lab-intro {
    margin: 40px 0;
    padding: 30px;
    background: #f8f9fa;
    border-radius: 10px;
  }
  .research-category {
    margin-top: 50px;
  }
  .research-category h2 {
    color: #333;
    border-bottom: 3px solid #4285f4;
    padding-bottom: 10px;
    margin-bottom: 30px;
  }
</style>

<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">
      <img src="{{ '/assets/img/1.jpg' | relative_url }}" alt="WDCC2025 Unitree Robot Opening">
    </div>
    <div class="swiper-slide">
      <img src="{{ '/assets/img/2.jpg' | relative_url }}" alt="WDCC2025 Unitree Robot Demonstration 2">
    </div>
    <div class="swiper-slide">
      <img src="{{ '/assets/img/3.jpg' | relative_url }}" alt="WDCC2025 Unitree Robot Demonstration 3">
    </div>
  </div>
  <!-- Add Pagination -->
  <div class="swiper-pagination"></div>
  <!-- Add Navigation -->
  <div class="swiper-button-next"></div>
  <div class="swiper-button-prev"></div>
</div>

<!-- Lab Introduction -->
<div class="lab-intro">
  <h2>About CDI Lab Robotics Group</h2>
  <p>
    The Living with Vision (LV) Group at CDI Lab is dedicated to exploring cutting-edge research in human-robot interaction, social robotics, and end-user programming. 
    Our research focuses on enabling robots to better understand human needs, designing more natural interaction interfaces, and empowering everyday users to easily program and customize robots.
  </p>
  <p>
    Our team consists of passionate researchers who believe that technology should serve humanity, making intelligent robots accessible and beneficial to everyone. 
    Through interdisciplinary collaboration and innovation, we are advancing the future of human-robot coexistence.
  </p>
</div>

<!-- Research Categories -->

<!-- Human Robot Communication -->
<div class="research-category">
  <h2>Human Robot Communication</h2>
  <div class="publications">
    {% bibliography --query @*[category=cdi-hrc] %}
  </div>
</div>

<!-- Social Robot -->
<div class="research-category">
  <h2>Social Robot</h2>
  <div class="publications">
    {% bibliography --query @*[category=cdi-social] %}
  </div>
</div>

<!-- End-User Programming -->
<div class="research-category">
  <h2>End-User Programming</h2>
  <div class="publications">
    {% bibliography --query @*[category=cdi-eup] %}
  </div>
</div>

<!-- Swiper JS -->
<script src="https://cdn.jsdelivr.net/npm/swiper@11.0.5/swiper-bundle.min.js"></script>
<script>
  var swiper = new Swiper('.swiper-container', {
    slidesPerView: 1,
    spaceBetween: 30,
    loop: true,
    autoplay: {
      delay: 3000,
      disableOnInteraction: false,
    },
    pagination: {
      el: '.swiper-pagination',
      clickable: true,
    },
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev',
    },
  });
</script>
