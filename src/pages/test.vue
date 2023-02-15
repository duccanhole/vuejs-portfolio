<template>
  <div class="underline font-bold">
    <button @click="show = !show">click:</button>
    <card v-if="show" />
  </div>
</template>
<script lang="ts" setup>
import { ref } from "@vue/reactivity";
import Card from "../components/Card.vue";

const show = ref(false);
</script>
