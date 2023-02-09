<template>
    <div class="reservation-block" :style="{width: totalWidth}"></div>
</template>

<script setup lang="ts">
import { computed } from "vue";

const props = defineProps<{
    hourWidth: number;
    startHour: number;
    endHour: number;
}>();

const reservationLength = computed(() => {
    return props.endHour - props.startHour;
});

const totalWidth = computed(() => {
    return reservationLength.value * props.hourWidth;
});
</script>

<style scoped lang="scss">
.reservation-block {
    height: 100%;
    background-color: #f00;
}
</style>