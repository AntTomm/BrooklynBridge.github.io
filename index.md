---
layout: default
title: Image Slideshow
---

<!--
A div with an id of 'slideshow' contains five images, the first of which is shown and the others are hidden using a display style of none. Using Javascript, create a simple slideshow that cycles through the images, displaying each image for three seconds at a time, looping back to the first image when the end is reached. You cannot use jQuery or any other library.
-->
<body>
<div id="slideshow">
	<img src="http://placehold.it/300x200&text=foo1.jpg">
	<img src="http://placehold.it/300x200&text=foo2.jpg" style="display: none">
	<img src="http://placehold.it/300x200&text=foo3.jpg" style="display: none">
	<img src="http://placehold.it/300x200&text=foo4.jpg" style="display: none">
	<img src="http://placehold.it/300x200&text=foo5.jpg" style="display: none">
</div>
<script>
var slideshow = document.getElementById('slideshow');
var slides = slideshow.getElementsByTagName('img');
var idx = 0;
function changeSlide() {
	slides[idx].style.display = 'none';
	idx = (idx + 1) % slides.length;
	slides[idx].style.display = 'block';
}
setInterval(changeSlide, 3000);
</script>
</body>
