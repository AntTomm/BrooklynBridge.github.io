---
layout: default
title: Simple Slideshow
---

# Simple Slideshow

<!-- Slideshow container with a fixed width to center the slideshow -->
<div id="slideshow" style="max-width: 300px; margin: 0 auto; border: 1px solid #ccc;">
  <img src="http://placehold.it/300x200&text=foo1.jpg" alt="foo1">
  <img src="http://placehold.it/300x200&text=foo2.jpg" alt="foo2" style="display: none">
  <img src="http://placehold.it/300x200&text=foo3.jpg" alt="foo3" style="display: none">
  <img src="http://placehold.it/300x200&text=foo4.jpg" alt="foo4" style="display: none">
  <img src="http://placehold.it/300x200&text=foo5.jpg" alt="foo5" style="display: none">
</div>

<script>
  // Grab the slideshow container and its images
  var slideshow = document.getElementById('slideshow');
  var slides = slideshow.getElementsByTagName('img');
  var idx = 0;

  // Function to hide the current slide and show the next one
  function changeSlide() {
      slides[idx].style.display = 'none';
      idx = (idx + 1) % slides.length;
      slides[idx].style.display = 'block';
  }

  // Change slide every 3 seconds
  setInterval(changeSlide, 3000);
</script>
