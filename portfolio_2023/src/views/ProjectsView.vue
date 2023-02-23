<script setup>
import { useRoute } from "vue-router";
import { ref, onMounted } from "vue";

let type = ref("");
const route = useRoute();

const scrollToTop = () => {
  window.scrollTo(0,0);
}

onMounted(() => {
  scrollToTop()
  type.value = route.params.type;
  console.log('type', type.value)
});
</script>
<template>
  <main>
    <div class="container mx-auto">
      <div class="row">
        <div class="col-4 offset-md-2" style="max-height: 359px">test</div>
        <div class="col-4" style="max-height: 359px">test</div>
      </div>
    </div>
  </main>
</template>
<style scoped></style>
