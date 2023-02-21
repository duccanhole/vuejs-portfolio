<template>
  <button
    ref="uiBtn"
    class="rounded-full p-3 text-yellow-300 border-2 border-dashed hover:border-dotted border-yellow-300 text-xl font-bold font-caveat relative"
    style="width: 150px; height: 150px"
    @click="onBtnClick"
  >
    <div class="bg-yellow-300 absolute animate__bounceIn"></div>
    <div>Start</div>
  </button>
</template>
<script lang="ts" setup>
import { ref } from "vue";
import sleep from "../shared/sleep";

const emit = defineEmits(["e:click"]);
const uiBtn = ref<HTMLButtonElement | null>(null);
async function onBtnClick() {
  uiBtn.value?.classList.add("ui-btn");
  const audio = new Audio("/sound-click.wav");
  audio.play();
  // emit("e:click", "asdasd");
  await sleep(2000);
  uiBtn.value?.classList.remove("ui-btn");
}
</script>
<style scoped>
.ui-btn > div:nth-child(1) {
  border-style: dotted;
  top: 0;
  left: 50%;
  transform: translate(-10px, -10px) rotate(45deg);
  /* border-radius: 60px; */
  width: 20px;
  height: 20px;
}
.ui-btn {
  animation: dots-move 2s forwards;
}
@keyframes dots-move {
  25% {
    transform: rotate(-35deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</style>
