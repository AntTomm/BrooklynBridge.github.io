---
layout: default
title: Image Slideshow
---

# Image Slideshow

<!-- Outer wrapper to control overall size and center the slideshow -->
<div style="max-width: 600px; margin: 0 auto; border: 1px solid #ccc;">
  <!-- Swiper container with fixed height -->
  <div class="swiper-container" style="width: 100%; height: 300px; position: relative;">
    <div class="swiper-wrapper">
      
      <!-- Slide #1 with the welcome image -->
      <div class="swiper-slide">
        <img
          src="{{ '/welcomeSign.jpeg' | relative_url }}"
          alt="Welcome Sign"
          style="max-width: 100%; height: auto; display: block; margin: 0 auto;"
        >
      </div>

      <!-- Slide #2 -->
      <div class="swiper-slide">
        <h3>Slide 2 content here</h3>
      </div>

      <!-- Slide #3 -->
      <div class="swiper-slide">
        <h3>Slide 3 content here</h3>
      </div>

    </div>

    <!-- Navigation & pagination controls -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
    <div class="swiper-pagination"></div>
  </div>
</div>

<!-- Swiper CSS & JS from CDN -->
<link rel="stylesheet" href="https://unpkg.com/swiper@latest/swiper-bundle.min.css">
<script src="https://unpkg.com/swiper@latest/swiper-bundle.min.js"></script>

<script>
  var mySwiper = new Swiper('.swiper-container', {
    slidesPerView: 1, // show one slide at a time
    loop: true,
    pagination: { el: '.swiper-pagination' },
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev',
    },
  });
</script>
