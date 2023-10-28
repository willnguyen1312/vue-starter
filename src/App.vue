<script setup>
import { ref, watchEffect } from 'vue';
import Comp from './Comp.vue';

const value = ref([1])

watchEffect(() => {
    // Nah
    console.log(value.value)
    // Reactive
    // console.log(value.value.length)
})
</script>

<template>
<Comp :value="value" />

<button @click="value = value.concat(value.length + 1)">Increment</button>
</template>