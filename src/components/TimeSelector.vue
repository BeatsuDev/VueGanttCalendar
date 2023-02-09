<template>
    <TimeSelectorRow v-for="name in roomNames"/>
</template>

<script setup lang="ts">
import TimeSelectorRow from "./TimeSelectorRow.vue";

const props = defineProps<{
  roomNames: string[];
}>();
</script>

<style scoped lang="scss">
</style>
