<template>
  <div class="px-9 py-8">
<Header :item="headings[0]"/>
<div class="flex gap-7">
  <div v-for="item in items.slice(0, 3)" :key="item.id">
  <div class="max-w-md w-full">
        <div
    class="rounded-2xl max-w-md border overflow-hidden hover:shadow-3xl">
    <div class="relative">
      <div class="absolute inset-0 bg-gradient-to-br  from-purple-400 to-indigo-600 opacity-75"></div>
      <img :src="item.image" alt="Product Image" class="w-full h-64 object-cover object-center relative z-10">
      <div
        class="absolute top-4 right-4 bg-[#DB4444] text-white text-xs font-bold px-3 py-2 rounded-full z-20 transform rotate-12">
        NEW</div>
    </div>
    <div class="p-6">
      <h2 class="text-3xl font-extrabold text-gray-800 mb-2">{{ item.title }}</h2>
      <p class="text-gray-600 mb-4">{{ item.description }}</p>
      <div class="flex items-center justify-between mb-4">
        <span class="text-2xl font-bold text-[#DB4444]">$299.99</span>
        <div class="flex items-center">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-yellow-400" viewBox="0 0 20 20"
            fill="currentColor">
            <path
              d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
          </svg>
          <span class="ml-1 text-gray-600">4.9 (120 reviews)</span>
        </div>
      </div>
      <button class="w-full bg-[#DB4444] text-white font-bold py-3 px-4 rounded-lg hover:bg-[#DB4444] transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-lg">
            Add to Cart
      </button>
    </div>
  </div>

</div>
</div>
</div>

<div class="py-5 flex justify-center">
 <NuxtLink to="/products"> <button class=" bg-[#DB4444] text-white font-bold py-3 px-8 rounded-sm hover:bg-[#DB4444] transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-lg">View All</button></NuxtLink>
</div>
  </div>
</template>

<script  setup>

const headings = [
  {title:"This Month",desc:"Best Selling Products"}
]

const items = [
{
  image: new URL('@/assets/jbsx.png', import.meta.url).href,
  title:"Cosmic Headphones",
  description:"Experience music like never before with our state-of-the-art Cosmic HeadphonesImmerse yourself in crystal-clear sound and unparalleled comfort.",
},
{
  image: new URL('@/assets/gameboy.png', import.meta.url).href,
  title:"Cosmic Headphones",
  description:"Experience music like never before with our state-of-the-art Cosmic HeadphonesImmerse yourself in crystal-clear sound and unparalleled comfort.",
},
{
  image: new URL('@/assets/camera.png', import.meta.url).href,
  title:"Cosmic Headphones",
  description:"Experience music like never before with our state-of-the-art Cosmic HeadphonesImmerse yourself in crystal-clear sound and unparalleled comfort.",
},
{
  image: new URL('@/assets/headphone.png', import.meta.url).href,
  title:"Cosmic Headphones",
  description:"Experience music like never before with our state-of-the-art Cosmic HeadphonesImmerse yourself in crystal-clear sound and unparalleled comfort.",
},

]
</script>

<style>

</style>