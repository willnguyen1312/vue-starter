<script setup lang="ts">
const props = defineProps<{
  input: number;
}>();

const emit = defineEmits<{
  changeStuff: [id: number];
}>();
</script>
