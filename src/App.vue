<script setup>
import { ref, watchEffect } from "vue";

function sleep(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

const first = ref(0);
const second = ref(0);

watchEffect(async () => {
  console.log("first run", first);
  // await sleep(1000);

  // second.value = first.value;
  // first.value = second.value;
});

function run() {
  first.value++;
}
</script>

<template>
  <div>
    <h1>Hi there</h1>
    <button @click="run">Click me</button>
    <p>First: {{ first }}</p>
    <p>Second: {{ second }}</p>
  </div>
</template>

<style scoped></style>
