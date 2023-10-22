<script setup>
import { ref, watch } from "vue";

function sleep(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

const first = ref(0);
const second = ref(0);

watch(first, async (newValue, oldValue) => {
  console.log("First changed from", oldValue, "to", newValue);
  console.log(second.value);
});
</script>

<template>
  <div>
    <h1>Hi there</h1>
    <button @click="first++">Increase first</button>
    <button @click="second++">Increase second</button>
    <p>First: {{ first }}</p>
    <p>Second: {{ second }}</p>
  </div>
</template>

<style scoped></style>
