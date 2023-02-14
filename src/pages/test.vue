<template>
  <div class="underline font-bold">
    This is Test page {{ count }}
    <button @click="count++">click:</button>
    <card />
  </div>
</template>
<script lang="ts" setup>
import { ref } from "@vue/reactivity";
import Card from "../components/Card.vue";

const count = ref(0);
</script>
