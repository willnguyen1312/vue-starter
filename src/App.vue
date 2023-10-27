<script setup>
import { ref } from 'vue';
import Comp from './Comp.vue';

const value = ref([1])
</script>

<template>
<Comp :value="value" />

<button @click="value.push(value.length + 1)">Increment</button>
</template>