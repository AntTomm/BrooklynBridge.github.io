---
layout: default
title: My Slideshow Page
---

# My Slideshow Page

<!-- A wrapper to control overall size/position -->
<div style="width: 600px; margin: 0 auto; border: 1px solid #ccc;">
  <!-- The actual Swiper container -->
  <div class="swiper-container" style="width: 100%; height: 300px; position: relative;">
    <div class="swiper-wrapper">
      <div class="swiper-slide">Slide 1</div>
      <div class="swiper-slide">Slide 2</div>
      <div class="swiper-slide">Slide 3</div>
    </div>
    
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
