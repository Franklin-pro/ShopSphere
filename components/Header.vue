<template>
    <div class="py-5">
      <h2 class="pl-3 border-l-8 border-[#DB4444] text-[#DB4444] font-bold">{{ props.item.title }}</h2>
      <div class="flex gap-4 pt-5 font-bold text-xl">
        <h1>{{ props.item.desc }}</h1>
        <h3>{{ props.item.time }}</h3>
      </div>
    </div>
</template>

<script lang="ts" setup>
interface Item {
  title: string;
  desc: string;
  time:string
}

const props = defineProps<{ item: Item }>();
</script>

<style>

</style>