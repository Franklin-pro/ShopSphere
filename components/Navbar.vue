<template>
  <div>
    <div class="flex border-b-2 justify-around items-center py-3 ">
      <div>
        <h1 class="font-black">SHOP-SPHERE</h1>
      </div>
        <nav>
          <div class="flex gap-8 font-semibold">
              <NuxtLink to="/" class="hover:underline">Home</NuxtLink>
              <NuxtLink to="/" class="hover:underline">Contacts</NuxtLink>
              <NuxtLink to="/" class="hover:underline">Abouts</NuxtLink>
          </div>
        </nav>
    
      <div class="flex items-center gap-6">
        <UInput size="lg" v-model="search" placeholder="Search ..."/>
        <UIcon name="i-heroicons-shopping-cart" class="text-xl cursor-pointer"/>
        <UIcon name="i-heroicons-heart" class="text-xl cursor-pointer"/>

        <UPopover :popper="{ arrow: true }">
          <UAvatar icon="i-heroicons-photo" size="sm" />

    <template #panel>
      <div class="p-4">
        <NuxtLink to="/">Create Account</NuxtLink>
      </div>
    </template>
  </UPopover>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

const search = ref("")

const links = [
  {label:"Home",path:"/"},
  {label:"Contact",path:"/"},
  {label:"About",path:"/"},
  {label:"Sign-Up",path:"/"},
]
</script>

<style>

</style>