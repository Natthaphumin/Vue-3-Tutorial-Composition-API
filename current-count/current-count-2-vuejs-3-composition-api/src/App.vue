<template>
  <main>
    <div>
      <h4>The current count is...</h4>
      <h1>{{ count }}</h1>
      <button @click="subtractFromCount()">-</button>
      <button @click="addToCount()">+</button>
    </div>
  </main>
</template>

<script setup>
import { ref } from "vue";

const count = ref(10);

const addToCount = () => {
  console.log("Add to count");
  count.value = count.value + 1;
};
const subtractFromCount = () => {
  console.log("subtract From count");
  count.value = count.value - 1;
};
</script>

<style scoped>
main {
  height: 100vh;
  max-width: 100vw;
  background-color: aliceblue;
  display: flex;
  align-items: center;
  justify-content: center;
}
div {
  text-align: center;
}
</style>
