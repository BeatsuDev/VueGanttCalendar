<template>
  <div id="container">
    <div id="sidebar">
      <RoomName :name=roomName v-for="roomName in props.roomNames"/>
    </div>
    <div id="main">
      <DateSelector />
      <TimeHeaderBar />
      <TimeSelector />
    </div>
  </div>
</template>

<script setup lang="ts">
import DateSelector from "./DateSelector.vue";
import TimeHeaderBar from "./TimeHeaderBar.vue";
import TimeSelector from "./TimeSelector.vue";
import RoomName from "./RoomName.vue";

const props = defineProps<{
  roomNames: string[];
}>();
</script>

<style scoped lang="scss">
#container {
  display: flex;
  flex-direction: row;
  height: 100%;
  width: 100%;
  background-color: $color-background;
  border-radius: 5px;
}

#sidebar {
  display: flex;
  flex-direction: column;
  min-width: 100px;
  max-width: 200px;
  background-color: $vt-c-black;
  border-radius: 5px 0 0 5px;
  padding: 10px 5px 10px 10px;
  text-align: right;
}
</style>
