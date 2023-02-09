<template>
  <div id="date-container">
    <div id="arrow-left" class="change-date-arrow">&lt;</div>
    <div id="date">Wednesday 18. September 2023</div>
    <div id="arrow-right" class="change-date-arrow">&gt;</div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
#date-container {
  display: flex;
  flex-direction: row;
  height: 40px;
  border-radius: 5px 5px 0 0;
  box-sizing: content-box;

  // Positioning
  justify-content: center;
  align-items: center;
  text-align: center;
  line-height: 40px;

  // Text styling
  font-size: 20px;
  background-color: $vt-c-black;
  border-bottom: 1px solid $vt-c-white;
}

// Styling the date and arrows
#date-container {
  .change-date-arrow {
    cursor: pointer;
    font-size: 30px;
    width: calc(100% - max(300px, calc(300px - 850px / (100 / 20) + 20vw)));  // Remove the width of the date
    transition-duration: 100ms;
    
    &:hover {
      color: $vt-c-white;
      background-color: $color-background-mute;
    }
  }

  // Fix the rounded borders
  #arrow-left {
    border-radius: 5px 0 0 0;
  }

  #arrow-right {
    border-radius: 0 5px 0 0;
  }

  #date {
    min-width: max(300px, calc(300px - 850px / (100 / 20) + 20vw));
  }
}
</style>
  