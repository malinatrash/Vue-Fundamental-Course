<script setup>
import CalculatorPage from "./Pages/CalculatorPage.vue";
import {computed, onBeforeMount, ref} from "vue";
import Student from "./Components/Student.vue";
const students = ref([])
const filterText = ref("")
onBeforeMount(async () => {
  let r = await fetch("students2022.json")
  let data = await r.json()
  students.value = data
})

const filteredStudents = computed(() => {
  return students.value.filter((s) => {
    return s.first_name.trim().toLowerCase().includes(filterText.value)
        || s.last_name.trim().toLowerCase().includes(filterText.value)
  })
})
</script>

<template>
  <div class="row m-2">
    <div class="col-12">
      <input placeholder="Поиск" type="text" class="form-control" v-model="filterText">
    </div>
  </div>
  <div v-for="student in filteredStudents">
    <Student :student="student"/>
  </div>
</template>

<style></style>