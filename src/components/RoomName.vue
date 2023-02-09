<template>
  <div>
    {{ props.name }}
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  name: string;
}>();
</script>

<style scoped lang="scss">
</style>
