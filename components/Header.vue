<template>
  <div class="py-8">
    <div class="flex w-2/3 justify-center ">
      <img src="../../../assets/images/logo/LeaziLogo.png" alt="">
    </div>
    <p class="text-4xl text-blue-500 font-semibold">{{ props?.item.title }}</p>
    <p class="text-md text-gray-900 font-thin mt-2 w-4/6">{{ props?.item.subtitle }}</p>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  item: Object
})
</script>

<style></style>