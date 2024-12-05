<template>
  <div>
    <Navbar/>
  </div>
  <div>
    <slot />
  </div>
  <div>
    <!-- <Footer/> -->
  </div>
</template>

<script lang="ts" setup>
import Footer from '~/components/Footer.vue';
</script>

<style>

</style>