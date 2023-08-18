<script>
export default {
  name: "PseudoProgressBar"
}
</script>

<script setup>
import { onBeforeMount } from 'vue';


const props = defineProps({
  text: String,
  value: String,
})

var width = '0%';

onBeforeMount(() => {
  width = props.value + '%';
})

</script>

<template>
  <div class="mb-6">
    <div class="flex justify-between font-sans font-medium text-lg">
      <span class="mb-1 font-medium text-white">{{ props.text }}</span>
      <span class="mb-1 font-medium text-white">{{ props.value }}%</span>
    </div>

    <div class="progress2 progress-moved w-full bg-bar-bg" h-1>
      <div class="progress-bar h-1" :style="`width: ${value}%`">
      </div>
    </div>
  </div>
</template>


<style scoped>
.progress-bar {
  transition: 0.4s linear;
  transition-property: width, background-color;
}

.progress-moved .progress-bar {
  background-color: white;
  animation: progressAnimation 6s;
}

@keyframes progressAnimation {
  0% {
    width: 0%;
    background-color: white;
  }

  100% {
    width: v-bind(width);
    background-color: white;
  }
}
</style>