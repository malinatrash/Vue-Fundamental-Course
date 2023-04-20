<script setup>
import {computed} from "vue";

const props = defineProps({
  student: {
    type: Object
  }
})

const url = computed(() => {
  return "vk.com/id" + props.student.id
})

</script>

<template>
  <div class="wrapper">
    <a :href="url" target="_blank">
      <img :src="student.photo_max_orig" alt="">
    </a>
      <h2>{{ student.first_name }} {{ student.last_name }}</h2>
    <span>{{ student.status }}</span>
  </div>
</template>


<style>
.wrapper {
  padding: 25px;
  margin: 30px;
  width: 450px;
  height: 100%;
  border: gainsboro solid 1px;
  border-radius: 25px;
}
img {
  margin: 10px;
  width: 150px;
  height: 150px;
  object-fit: cover;
  border-radius: 90px;
}
</style>