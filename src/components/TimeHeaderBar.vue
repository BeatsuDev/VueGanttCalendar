<template>
  <div id="time-header">
    <div class="time-hour" v-for="hour in hours">{{ hour }}</div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  startHour: number;
}>();

let normalHours = Array.from({ length: 24 }, (_, i) => ("00" + i).slice(-2));
const hours = normalHours.slice(props.startHour).concat(normalHours.slice(0, props.startHour));
</script>

<style scoped lang="scss">
#time-header {
  display: flex;
  flex-direction: row;
  height: 20px;
  padding: 4px;
  line-height: 12px;

  // Text styling
  font-size: 14px;
  background-color: $vt-c-black;

  .time-hour {
    width: calc(100% / 24);
    text-align: center;
  }
}
</style>
