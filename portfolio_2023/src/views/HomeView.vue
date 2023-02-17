<script setup></script>

<template>
  <main class="container mx-auto" style="margin-top: -150px">
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
      <a class="text-navy font-weight-600"><u>Télécharger mon cv 🔥</u></a>
    </div>
    <div class="row">
      <div
        data-aos="slide-up"
        data-aos-easing="linear"
        data-aos-duration="1000"
        class="purple-bloc mt-1"
      >
        <h1><i>Mes projets web</i></h1>
        <img class="img-class" src="../assets/img/web.svg" />
      </div>
      <div
        class="blue-bloc mt-2"
        data-aos="slide-up"
        data-aos-easing="linear"
        data-aos-duration="1500"
      >
        <img class="img-class" src="../assets/img/ui.svg" />
        <h1><i>Mes conceptions UI</i></h1>
      </div>
    </div>
  </main>
</template>
