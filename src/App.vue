<script setup lang="ts">
import GanttCalendar from "./components/GanttCalendar.vue";

const rooms: string[] = [
  "Storsalen",
  "Klubben",
  "Knaus",
  "Rundhallen",
  "Edgar",
  "Lyche",
  "Bodegaen",
  "Biblioteket",
  "Strossa",
  "Selskapssiden",
  "Talekoffert 1",
  "Talekoffert 2",
  "Talekoffert 3",
  "Trafon, Nedre Møterom",
  "Trafon, Øvingsrom",
  "Låneprosjektor",
];
</script>

<template>
  <GanttCalendar :room-names="rooms"/>
</template>

<style scoped>

</style>
