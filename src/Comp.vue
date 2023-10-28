<script setup>
import { computed, watch, watchEffect } from 'vue';

const props = defineProps({
    value: Array
})

const display = computed(() => props.value.length * 2)

watch(props, () => {
    // console.log(props.value)
})
</script>

<template>
    <h1>Display: {{ display }}</h1>
</template>