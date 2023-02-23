<script setup>
import { useRoute } from "vue-router";
import { ref, onMounted } from "vue";

let type = ref("");
const route = useRoute();

onMounted(() => {
  type.value = route.params.type;
  console.log(type.value);
});
</script>
<template>
  <div class="row">
    <div class="col-12"><p>test</p></div>
  </div>
</template>
<style scoped></style>
