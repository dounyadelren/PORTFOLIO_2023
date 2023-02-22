<script setup></script>
<template>
  <div id="sidebar" class="col-1 d-flex flex-column justify-content-center ms-2 position-sticky">
    <a href=""><img  class="side-logo mb-1" data-aos="fade-right" data-aos-duration="1000" src="../assets/img/github.png" /></a>
    <a href=""><img  class="side-logo mb-1" data-aos="fade-right" data-aos-duration="1500" src="../assets/img/linked.png" /></a>
    <a href=""><img  class="side-logo mb-1" data-aos="fade-right" data-aos-duration="2000" src="../assets/img/mail.png" /></a>
  </div>
</template>
<style scoped>
.side-logo {
	width: 30px;
	height: 30px;
}
img.side-logo:hover {
	transition: transform 0.3s;
  transform: scale(1.090);
}
#sidebar {
	top: 50%;
	z-index: 99999
}
</style>
