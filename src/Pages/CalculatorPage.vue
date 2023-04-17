<script setup>
import { ref, computed } from 'vue'
import Operationbutton from "../Components/Operationbutton.vue";
const OPERATIONS = ['+', '-', '*', '/']
let a = ref(11)
let b = ref(20)
let c = computed(() => {
  switch (operation.value) {
    case '+':
      return a.value + b.value
    case '-':
      return a.value - b.value
    case '/':
      return a.value / b.value
    case '*':
      return a.value * b.value
  }
})
let operation = ref('+')
const setOp = value => {
  operation.value = value
}
</script>

<template>
  <div class="container">
    <input
        type="number"
        class="form-control frm"
        v-model="a"
    />
    <input
        type="number"
        class="form-control frm"
        v-model="b"
    />
    <div class="row mt-2">
      <div
          class="col-3"
          v-for="op in OPERATIONS"
      >
        <Operationbutton
            @clicked="setOp(op)"
            :operation="op"
        />
      </div>
    </div>
    <hr />
    <h1>{{ a }} {{ operation }} {{ b }} = {{ c }}</h1>
  </div>
</template>

<style>
.container {
  margin-top: 15px;
}
.frm {
  margin-top: 15px;
}
</style>
