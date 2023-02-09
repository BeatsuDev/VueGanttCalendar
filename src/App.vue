<script setup lang="ts">
import GanttCalendar from "./components/GanttCalendar.vue";

const rooms: string[] = ["Bodega", "Lyche", "Bakrommene", "Kjøkken", "Et jævlig langt navn for et rom"];
</script>

<template>
  <GanttCalendar :room-names="rooms"/>
</template>

<style scoped>

</style>
