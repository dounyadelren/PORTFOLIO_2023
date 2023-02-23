<script setup>
import { useRoute } from "vue-router";
import { onMounted } from "vue";
import { watch, ref } from "vue";
import router from "../router";

const route = useRoute();
const navbarUn = ref(true);
const navbarDeux = ref(false);
let type = ref("");
onMounted(() => {
  type.value = route.params.type;
});

watch(
  () => route.path,
  () => {
    console.log(route.path);
    if (route.path == "/projects/web" || route.path == "/projects/ui") {
      navbarDeux.value = true;
      navbarUn.value = false;
    } else {
      navbarDeux.value = false;
      navbarUn.value = true;
    }
  }
);

const redirect = (route) => {
  router.push("/projects/" + route);
};
</script>
<template>
  <div>
    <nav class="navbar font-12">
      <div class="">
        <a href="/"
          ><img src="../assets/img/LogoDD.png" class="logo-class"
        /></a>
      </div>
      <div
        v-if="navbarUn"
        class="d-flex align-items-center cursor menu-container justify-content-around"
      >
        <a href="#web" v-smooth-scroll class="menu-item me-2 letter-space-1"
          >Mes projets webs</a
        >
        <a href="#ui" v-smooth-scroll class="menu-item me-2 letter-space-1"
          >Mes conceptions UI</a
        >
      </div>
      <div
        v-if="navbarDeux"
        class="d-flex align-items-center cursor menu-container justify-content-around"
      >
        <p @click="redirect('web')" class="menu-item me-2 letter-space-1">
          Mes projets webs
        </p>
        <p @click="redirect('ui')" class="menu-item me-2 letter-space-1">
          Mes conceptions UI
        </p>
      </div>
      <div class="d-flex align-items-center">
        <button id="contact-btn">Me contacter</button>
      </div>
    </nav>
  </div>
</template>
<style></style>
