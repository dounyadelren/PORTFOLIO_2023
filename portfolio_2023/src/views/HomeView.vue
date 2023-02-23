<script setup>
import { ref, onMounted, reactive } from "vue";
import Bloc from "../components/Bloc.vue";
import Web from "../assets/img/web.svg";
import Ui from "../assets/img/ui.svg";

onMounted(() => {});

const webProjects = reactive([
  {
    id: "web",
    title: "Mes projets web",
    img: Web,
    class: "purple-bloc",
    duration: "700",
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
      {
        date: "2021",
        name: "Ancien portfolio",
        route: "/",
        techno: "React JS",
      },
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
    duration: "1000",
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
  <main>
    <div class="container mx-auto">
      <div class="row">
        <div class="col-4 offset-md-2" style="max-height: 359px">
          <h1 class="letter-space-2 text-purple font-50 bold mb-1">Hello,</h1>
          <h2 class="font-weight-300 letter-space-1 mb-1 text-secondary">
            Je m'appelle Dounya,
          </h2>
          <h3 class="font-weight-300 letter-space-0 mb-2 text-secondary">
            je suis
            <span class="text-purple font-weight-600">développeuse web</span> et
            <span class="text-purple font-weight-600">UX/UI designer</span>
          </h3>
          <div class="row">
            <a class="text-green font-weight-600 link"
              ><u>Télécharger mon cv 🔥</u></a
            >
          </div>
          <div class="row not-opaque">
            <div class="col-12 d-flex flex-row">
              <div
                data-aos="zoom-in"
                data-aos-easing="ease-in-back"
                data-aos-delay="130"
              >
                <img class="me-1 tiny-logo" src="../assets/img/figma.svg" />
              </div>
              <div
                data-aos="zoom-in"
                data-aos-easing="ease-in-back"
                data-aos-delay="120"
              >
                <img class="me-1 tiny-logo" src="../assets/img/vue.svg" />
              </div>
              <div
                data-aos="zoom-in"
                data-aos-easing="ease-in-back"
                data-aos-delay="110"
              >
                <img class="me-1 tiny-logo" src="../assets/img/css.svg" />
              </div>
              <div
                data-aos="zoom-in"
                data-aos-easing="ease-in-back"
                data-aos-delay="100"
              >
                <img class="me-1 tiny-logo" src="../assets/img/procreate.svg" />
              </div>
            </div>
          </div>
        </div>
        <div class="col-4" style="max-height: 359px">
          <div
            class="bg-blob"
            data-aos="fade-zoom-out"
            data-aos-easing="ease-in-back"
            data-aos-delay="1000"
            data-aos-offset="0"
            data-aos-duration="6000"
          ></div>
        </div>
        <div class="col-12">
          <div class="bg-orange">
            <div class="blur"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="row justify-content-center align-items-center m-3" data-aos="fade-down" data-aos-delay="500">
      <img id="arrow" src="../assets/img/arrow.png" />
    </div>
    <div class="row justify-content-center mx-auto align-items-center">
      <Bloc :test="webProjects" />
      <Bloc :test="uiProjects" />
    </div>
  </main>
</template>
