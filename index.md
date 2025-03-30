---
layout: default
title: Image Slideshow
---

# Image Slideshow

<!-- A wrapper to control overall size/position -->
<div style="width: 600px; margin: 0 auto; border: 1px solid #ccc;">
  <!-- The actual Swiper container -->
  <div class="swiper-container" style="width: 100%; height: 300px; position: relative;">
    <div class="swiper-wrapper">
      <!-- Slide 1 with an image -->
      <div class="swiper-slide">
        <img
          src="{{ '/welcomeSign.jpeg' | relative_url }}"
          alt="Welcome Sign"
          style="max-width: 100%; height: auto; display: block;"
        >
      </div>
      <!-- Slide 2 -->
      <div class="swiper-slide">
        Slide 2 content here
      </div>
      <!-- Slide 3 -->
      <div class="swiper-slide">
        Slide 3 content here
      </div>
    </div>

    <!-- Swiper controls -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
    <div class="swiper-pagination"></div>
  </div>
</div>



<!-- Swiper JS & CSS from CDN -->
<link
  rel="stylesheet"
  href="https://unpkg.com/swiper@latest/swiper-bundle.min.css">
<script src="https://unpkg.com/swiper@latest/swiper-bundle.min.js"></script>

<script>
  var mySwiper = new Swiper('.swiper-container', {
    loop: true,
    pagination: { el: '.swiper-pagination', },
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev',
    },
  });
</script>
