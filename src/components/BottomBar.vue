<template>
  <div
    class="fixed bottom-0 w-screen flex justify-around"
    style="height: 100px"
  >
    <div
      class="rounded-full bg-gray-200 -translate-y-14"
      style="width: 100px; height: 100px"
    >
        Info
    </div>
    <div
      class="rounded-full bg-gray-200 -translate-y-10"
      style="width: 100px; height: 100px"
    >
        Project
    </div>
    <div
      class="rounded-full bg-gray-200 -translate-y-10"
      style="width: 100px; height: 100px"
    >
        Contact
    </div>
  </div>
</template>
<script lang="ts" setup></script>
<style scoped>
.nav-item::before {
    content: "";
    width: 40px;
    height: 20px;
    background-color: #eab308;
    position: absolute;
    bottom: 20px;
    left: -45px;
    border-top-right-radius: 50%;
    border-top-left-radius: 40%;
}
</style>
