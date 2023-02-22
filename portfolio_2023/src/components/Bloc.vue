<script setup>
import { ref } from "vue";
import { Collapse } from "vue-collapsed";

const props = defineProps({
  test: Array,
});

const isDropped = ref(false);

const displayProject = () => {
  isDropped.value = !isDropped.value;
};
</script>
<template>
  <div
    :id="props.test[0].id"
    data-aos="slide-up"
    data-aos-easing="linear"
		data-aos-once="true"
    :data-aos-duration="props.test[0].duration"
    :class="props.test[0].class + ' mt-2 cursor row'"
  >
    <h1 @click="displayProject">
      <i>{{ props.test[0].title }}</i>
    </h1>
    <img class="img-class" :src="props.test[0].img" />
  </div>
  <Collapse :when="isDropped" class="v-collapse w-100">
    <ul :class="(props.test[0].id === 'projects' ? 'bg-purple' : 'bg-blue') + ' list-collapsed mx-auto'">
      <li
        class="list-item d-flex justify-between align-items-center"
        v-for="project in props.test[0].projects"
        :key="project.name"
      >
        <a :href="props.test[0].route">{{project.date + " - " +  project.name }}</a><p class="font-12">{{ project.techno }}</p>
      </li>
    </ul>
  </Collapse>
</template>
<style scoped>
.v-collapse {
  transition: height var(--vc-auto-duration) cubic-bezier(0.33, 1, 0.68, 1);
}
.list-collapsed {
  padding: 0.5rem;
  padding-left: 4rem;
  padding-right: 4rem;
  margin-top: 0.5rem;
  /* background: var(--lightpurple); */
	border-radius: 10px;
}

.list-collapsed .list-item {
  padding-top: 0.5rem;
	padding-bottom: 0.5rem;
}

.list-collapsed .list-item:hover {
  color: var(--orange)
}
</style>
