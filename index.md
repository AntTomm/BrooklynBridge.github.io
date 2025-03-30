---
layout: default
title: Simple Slideshow
---

# Simple Slideshow

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Simple Slideshow</title>
  <style>
    /* Style the slideshow container */
    #slideshow {
      max-width: 600px;
      margin: 50px auto;
      position: relative;
      overflow: hidden;
      border: 2px solid #333;
    }
    /* Style each slide image */
    #slideshow img {
      width: 100%;
      display: none; /* Hide all images by default */
      position: absolute;
      top: 0;
      left: 0;
    }
    /* Only display the active slide */
    #slideshow img.active {
      display: block;
    }
  </style>
</head>
<body>

<div id="slideshow">
  <img src="https://via.placeholder.com/600x400?text=Slide+1" alt="Slide 1" class="active">
  <img src="https://via.placeholder.com/600x400?text=Slide+2" alt="Slide 2">
  <img src="https://via.placeholder.com/600x400?text=Slide+3" alt="Slide 3">
  <img src="https://via.placeholder.com/600x400?text=Slide+4" alt="Slide 4">
  <img src="https://via.placeholder.com/600x400?text=Slide+5" alt="Slide 5">
</div>

<script>
  // Wait for the DOM to load
  document.addEventListener('DOMContentLoaded', function() {
    var slides = document.querySelectorAll('#slideshow img');
    var currentSlide = 0;
    
    // Function to move to the next slide
    function nextSlide() {
      slides[currentSlide].classList.remove('active');
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].classList.add('active');
    }
    
    // Change slide every 3 seconds
    setInterval(nextSlide, 3000);
  });
</script>

</body>
</html>
