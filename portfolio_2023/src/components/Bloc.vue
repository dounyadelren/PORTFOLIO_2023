<script setup>
import { ref, onMounted } from "vue";
import Loader from "../components/Loader.vue"
import { useRoute } from "vue-router";
import router from '../router'

const isLoading = ref(false)
const isDone = ref(false)
const route = useRoute()
const props = defineProps({
  test: Array,
});
const isDropped = ref(false);

const displayProject = () => {
  isDropped.value = !isDropped.value;
};

const redirect = (route) => {
  setTimeout(() => {
    isLoading.value = true
    isDone.value = true
  }, 1000)
  setTimeout(() => {
    if (isDone.value === true) {
      isLoading.value = false
      router.push('/projects/' + route)
    }
  }, 4000)
}

onMounted(()=> {
  console.log(isLoading.value)
})
</script>
<template>
  <Loader v-if="isLoading" />
  <div
    v-else
    @click="redirect(props.test[0].id)"
    :id="props.test[0].id"
    data-aos="slide-up"
    data-aos-easing="linear"
    data-aos-once="true"
    :data-aos-duration="props.test[0].duration"
    :class="props.test[0].class + ' mt-4 cursor col-12'"
  >
    <h1 @click="displayProject" class="font-30 text-secondary">
      <span class="font-weight-bold">{{ props.test[0].title.substr(0, 1) }}</span>
      <span class="font-weight-300">{{ props.test[0].title.substr(1) }}</span>
    </h1>
    <img class="img-class" :src="props.test[0].img" />
  </div>
</template>
<style scoped>
</style>
