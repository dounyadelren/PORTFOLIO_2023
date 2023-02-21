<script setup>
import { ref, onMounted, reactive } from "vue";
import Bloc from "../components/Bloc.vue";
import Web from "../assets/img/web.svg";
import Ui from "../assets/img/ui.svg";

onMounted(() => {});

const webProjects = reactive([
  {
    id: "projects",
    title: "Mes projets web",
    img: Web,
    class: "purple-bloc",
    duration: "1000",
    projects: [
      {
        date: "2023",
        name: "Camping vs Wild",
        route: "/",
        techno: "Vue JS, Ruby On Rails",
      },
      {
        date: "2022",
        name: "Previously On",
        route: "/",
        techno: "React JS, Express",
      },
      {
        date: "2022",
        name: "Mak'o - projet e-commerce",
        route: "/",
        techno: "React JS, Symphony",
      },
      { date: "2021", name: "Ancien portfolio", route: "/", techno: "React JS" },
      {
        date: "2021",
        name: "Snapchat",
        route: "/",
        techno: "React Native, Expo",
      },
      { date: "2021", name: "Twitter", route: "/", techno: "PHP, JQuery" },
    ],
  },
]);

const uiProjects = reactive([
  {
    id: "ui",
    title: "Mes conceptions ui",
    img: Ui,
    class: "blue-bloc",
    duration: "1500",
    projects: [
      { date: "2023", name: "Rocket Feed", route: "/", techno: "Figma" },
      { date: "2023", name: "Ce portfolio", route: "/", techno: "Figma" },
      {
        date: "2022",
        name: "Glassmorphism",
        route: "/",
        techno: "Figma, Youtube",
      },
      {
        date: "2022",
        name: "Toggle light/dark",
        route: "/",
        techno: "Figma, Youtube",
      },
      {
        date: "2022",
        name: "Mak'o - Projet e-commerce",
        route: "/",
        techno: "Figma",
      },
      { date: "2021", name: "Omega Gaming", route: "/", techno: "Figma" },
    ],
  },
]);
</script>

<template>
  <main class="container mx-auto" style="margin-top: -130px">
    <div class="row mb-2">
      <div class="col-5">
        <h1 class="letter-space-2 text-orange font-50 bold mb-1">Hello,</h1>
        <h2 class="font-weight-400 letter-space-1 mb-1">
          Je m'appelle Dounya,
        </h2>
        <h3 class="font-weight-400 letter-space-0 mb-2">
          je suis
          <span class="text-navy font-weight-600">développeuse web</span> et
          <span class="text-navy font-weight-600">UX/UI designer</span>
        </h3>
        <img class="mr-1 tiny-logo" src="../assets/img/figma.svg" />
        <img class="mr-1 tiny-logo" src="../assets/img/vue.svg" />
        <img class="mr-1 tiny-logo" src="../assets/img/css.svg" />
        <img class="mr-1 tiny-logo" src="../assets/img/procreate.svg" />
      </div>
      <div class="col-5 ml-5">
        <div class="bg-blob"></div>
      </div>
    </div>
    <div class="row">
      <a class="text-navy font-weight-600 link"><u>Télécharger mon cv 🔥</u></a>
    </div>
    <div class="row">
      <Bloc :test="webProjects" />
      <Bloc :test="uiProjects" />
    </div>
  </main>
</template>
