<template>
  <button
    class="rounded-full p-3 bg-gray-300 text-lg font-bold font-caveat hover:bg-gradient-to-br hover:from-gray-300 hover:via-lime-300 hover:to-green-300 hover:shadow-xl transition ui-btn"
    @click="onBtnClick"
  >
    Start
  </button>
</template>
<script lang="ts" setup>
function onBtnClick() {
  const audio = new Audio("/sound-click.wav");
  audio.play();
}
</script>
<style scoped>
.ui-btn:active {
  animation: border-move 0.4s;
}
@keyframes border-move {
  0% {
    border-top: 5px solid #15803d;
    border-right: none;
    border-bottom: none;
    border-left: none;
  }
  25% {
    border-top: 2px solid #22c55e;
    border-right: 5px solid #15803d;
    border-bottom: none;
    border-left: none;
  }
  50% {
    border-top: none;
    border-right: 2px solid #22c55e;
    border-bottom: 5px solid #15803d;
    border-left: none;
  }
  100% {
    border-top: none;
    border-right: none;
    border-bottom: 2px solid #22c55e;
    border-left: 5px solid #15803d;
  }
}
</style>
