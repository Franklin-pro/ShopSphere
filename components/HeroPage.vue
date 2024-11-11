<script setup lang="ts">
const links = [
  [{
    label: 'Franklin',
    avatar: {
      src: 'https://avatars.githubusercontent.com/u/739984?v=4'
    },
  }, {
    label: 'Women Fashion',
    to: '/getting-started/installation',
    subItem :[
{ 
  sublabel: 'Men Fashion',
    icon: 'i-heroicons-home',
  }
    ]
  },
  {
    label: 'Medicine',
    to: '/getting-started/installation',
  },
  {
    label: 'Sports & OutDoor',
    to: '/getting-started/installation',
  },
  
  {
    label: 'Electronics',
    to: '/components/vertical-navigation',
  }, {
    label: 'Groceries & Pets',
    to: '/components/command-palette',
    subItem :[
{ 
  sublabel: 'Installation',
    icon: 'i-heroicons-home',
  }
    ]
  }], [{
    label: 'Health & Beauty',
  }, {
    label: 'Help',
  }]
]

const isOpen = ref(false)
</script>

<template>
  <div class="flex px-5 justify-around py-4">
    <div class=" max-sm:hidden">
      <UVerticalNavigation :links="links"  />
    </div>

    <section class="px-3 py-5 bg-black max-sm:w-full max-sm:bg-transparent lg:py-10">
    <div class="grid lg:grid-cols-2 items-center justify-items-center gap-5">
        <div class="order-2 lg:order-1 flex flex-col justify-center pl-6">
          <h3 class="text-xl font-bold md:text-2xl text-white ">IPhone 14 pro series</h3>
            <p class="text-3xl text-white  font-bold md:text-7xl">25% OFF</p>
            <p class="text-3xl text-white  font-bold md:text-7xl">SUMMER SALE</p>
            <p class="mt-2 text-white  text-sm md:text-lg">For limited time only!</p>
            <NuxtLink to="/" class="pt-4 underline flex items-center gap-2">Shop Now <UIcon name="i-heroicons-arrow-right"/></NuxtLink>
        </div>
        <div class="order-1 lg:order-2">
            <img class="h-80 w-80 object-cover lg:w-[500px] lg:h-[500px]" src="../assets/heroImage.png" alt="">
        </div>
    </div>
</section>
  </div>

</template>



<style>

</style>