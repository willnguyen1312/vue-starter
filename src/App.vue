<script setup>
import MemoryGame from "./MemoryGame.vue";
</script>

<template>
  <MemoryGame :rows="2" :cols="2" :delay="2000" :matchCount="2" />
</template>
