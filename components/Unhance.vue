<template>
  <div class="p-9">
    <section class="px-3 py-5 bg-black max-sm:w-full rounded-2xl max-sm:bg-transparent lg:py-10">
    <div class=" gap-5">
      <div v-for="item in discount">
        <div class="flex justify-between items-center">
          <div class="order-2 lg:order-1 flex flex-col justify-center pl-6">
          <h3 class="text-xl font-bold md:text-xl text-[#00FF66] ">{{ item.title }}</h3>
            <p class="mt-2 text-3xl text-white  font-bold md:text-7xl">{{ item.desc }}</p>
            <div class="pt-5">
              <button class="bg-[#00FF66] py-2 px-9 font-semibold rounded-md hover:bg-[#DB4444] transition duration-300 ease-in-out transform hover:-translate-y-1">Shop Now!</button>
            </div>
        </div>
        <div class="order-1 lg:order-2">
            <img class=" object-cover " :src="item.image" alt="">
        </div>
        </div>
     
      </div>
   
    </div>
</section>
  </div>
</template>

<script lang="ts" setup>
const discount = [
  {
    image: new URL('@/assets/jbsx.png', import.meta.url).href,title:"categories",desc:"Enhance Your Music Experience"
  }
]
</script>

<style>

</style>