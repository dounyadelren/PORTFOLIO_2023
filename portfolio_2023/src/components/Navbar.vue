<script setup>
</script>
<template>
  <div>
    <nav class="navbar font-12">
      <div class="">
        <a href="/" ><img src="../assets/img/LogoDD.png" class="logo-class" /></a>
      </div>

      <div class="d-flex align-items-center cursor menu-container justify-content-around">
        <a href="#web" v-smooth-scroll class="menu-item me-2 letter-space-1">Mes projets webs</a>
        <a href="#ui" v-smooth-scroll class="menu-item me-2 letter-space-1">Mes conceptions UI</a>
        <!-- <a href="#cv" v-smooth-scroll class="menu-item letter-space-1">Mon parcours</a> -->
      </div>

      <div class="d-flex align-items-center">
        <button id="contact-btn">Me contacter</button>
      </div>
    </nav>
  </div>
</template>
<style>
</style>
