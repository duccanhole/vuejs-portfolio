<template>
  <div
    class="rounded-lg cursor-pointer p-2 hover:shadow-2xl hover:-translate-y-6 transition"
    :style="{ width: '250px', height: '300px' }"
  >
    <div
      class="bg-pink-200 border-4 border-pink-500 rounded-lg h-full flex flex-col justify-center relative"
    >
      <div
        class="absolute left-0 top-0 bg-pink-500 rounded-br-md px-2 font-caveat font-bold text-white"
      >
        intro
      </div>
      <div
        class="absolute bottom-0 right-0 bg-pink-500 rounded-br-md px-2 font-caveat font-bold text-white rotate-180"
      >
        intro
      </div>
      <div class="absolut inset-0">
        <img
          src="https://www.liblogo.com/img-logo/ad381aad4-adobe-illustrator-logo-adobe-illustrator-logo-free-icon-of-vector-logo.png"
        />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
const props = defineProps({
  propA: String,
});
console.log(props.propA);
</script>
