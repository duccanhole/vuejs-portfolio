<template>
  <div class="h-screen grid place-content-center bg-cyan-600 relative">
    <div
      class="text-center grid place-content-center w-80 h-80 shadow-xl rounded-full bg-teal-700"
    >
      <ui-button @e:click="onStart" />
    </div>
    <div class="block-1"></div>
    <div class="block-2"></div>
    <div class="block-3"></div>
  </div>
</template>
<script lang="ts" setup>
import { ref } from "@vue/reactivity";
import Card from "../components/Card.vue";
import UiButton from "../components/UiButton.vue";
async function onStart() {}
function sleep(ms: number) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}
</script>
<style scoped>
.block-1, .block-2, .block-3 {
  position: absolute;
  width: 100px;
  height: 100px;
  background-color: black;
}
.block-1 {
  top: 5%;
  left: 10%;
}
.block-2 {
  right: 5%;
  top: 30%;
}
.block-3 {
  bottom: 8%;
  left: 22%;
}
</style>
