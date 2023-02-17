<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Navbar from "../src/components/Navbar.vue"
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <Navbar />
        <!-- <RouterLink to="/">Home</RouterLink> -->
      </nav>
    </div>
  </header>
  <RouterView />
</template>