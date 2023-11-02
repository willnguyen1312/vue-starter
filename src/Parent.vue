<script setup lang="ts">
import Child from "./Child.vue";

type Props = InstanceType<typeof Child>["$props"];
</script>

<template>
  <Child :input="123" />
</template>
