<template>
  <div class="px-9 py-8">
    <Header :item="headings[0]"/>
    <div class="flex justify-center gap-6">
    <div v-for="item in category" :key="item.id">
      <div class="border bg-slate-400 rounded-md hover:bg-red-500 duration-500 cursor-pointer text-white px-7 py-2">
        <img :src="item.image" alt="categories">
        <span>{{ item.title }}</span>
      </div>
    </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

const headings = [
  {title:"Categories",desc:"Browse by Categories",time:"2 Days Remain"}
]

const category = [
  {id:"1", image: new URL('@/assets/camera.png', import.meta.url).href, title:"camera"},
  {id:"2", image: new URL('@/assets/cellPhone.png', import.meta.url).href, title:"TV"},
  {id:"3", image: new URL('@/assets/computer.png', import.meta.url).href, title:"Phone"},
  {id:"4", image: new URL('@/assets/gamepad.png', import.meta.url).href, title:"clothes"},
  {id:"5", image: new URL('@/assets/headphone.png', import.meta.url).href, title:"shoes"},
];



</script>

<style>

</style>