<template>
  <div id="room-name">
    {{ props.name }}
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  name: string;
}>();
</script>

<style scoped lang="scss">
#room-name {
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow: hidden;
  padding: 1px 0;
}
</style>
