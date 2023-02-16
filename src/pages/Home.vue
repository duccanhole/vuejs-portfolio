<template>
  <div class="h-screen flex flex-col justify-center">
    <div class="text-center"><ui-button /></div>
    <!-- <card v-if="show" prop-a="hello" /> -->
  </div>
</template>
<script lang="ts" setup>
import { ref } from "@vue/reactivity";
import Card from "../components/Card.vue";
import UiButton from "../components/UiButton.vue";
const show = ref(false);
</script>
