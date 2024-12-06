<template>
  <div class="bg-gray-100">
 
    <div class="carousel-container relative overflow-hidden rounded-lg">
      <div>
      <Header :item="title"/>
    </div>
    <div
      class="carousel-wrapper flex transition-transform duration-500"
      :style="{ transform: `translateX(-${activeIndex * 100}%)` }" 
    >
      <div
      v-if="filteredBlogs.length > 0"
        v-for="(item, index) in filteredBlogs"
        :key="item.id"
        class="carousel-item w-full lg:w-1/3 flex-shrink-0 p-4"
      >
       

<div class="w-full  max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
    <a href="#" class="w-[400px] h-[300px]">
        <img class=" rounded-t-lg w-full object-cover object-top-center h-[300px]" :src="item.blogImage?.url" alt="product image" />
    </a>
    <div class="px-5 pb-5">
        <a href="#">
            <h5 class="text-xl font-semibold tracking-tight text-gray-900 dark:text-white">{{ item.blogName }}</h5>
        </a>
        <div class="flex items-center mt-2.5 mb-5">
            <div class="flex items-center space-x-1 rtl:space-x-reverse">
                <svg class="w-4 h-4 text-yellow-300" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 22 20">
                    <path d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z"/>
                </svg>
                <svg class="w-4 h-4 text-yellow-300" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 22 20">
                    <path d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z"/>
                </svg>
                <svg class="w-4 h-4 text-yellow-300" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 22 20">
                    <path d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z"/>
                </svg>
                <svg class="w-4 h-4 text-yellow-300" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 22 20">
                    <path d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z"/>
                </svg>
                <svg class="w-4 h-4 text-gray-200 dark:text-gray-600" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 22 20">
                    <path d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z"/>
                </svg>
            </div>
            <span class="bg-blue-100 text-blue-800 text-xs font-semibold px-2.5 py-0.5 rounded dark:bg-blue-200 dark:text-blue-800 ms-3">5.0</span>
        </div>
        <div class="flex items-center justify-between">
            <span class="text-3xl font-bold text-gray-900 dark:text-white">$599</span>
            <a href="#" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Add to cart</a>
        </div>
    </div>
</div>

      </div>
      <template v-else>
              <div v-for="n in 6" :key="n" class="p-5 dark:bg-gray-700 bg-white rounded-xl">
                <div class="relative lg:mb-12">
                  <USkeleton class="h-[300px] w-[400px]" :ui="{ rounded: 'rounded-md' }" />
                </div>
                <div class="space-y-4">
                  <USkeleton class="h-8 w-[300px]" />
                  <USkeleton class="h-4 w-[250px]" />
                  <USkeleton class="h-4 w-[280px]" />
                  <USkeleton class="h-4 w-[120px]" />
                </div>
              </div>
            </template>
    </div>
    <!-- Previous and Next buttons -->
    <UButton @click="prevSlide" icon="i-heroicons-chevron-left" class="absolute left-0 top-1/2 transform -translate-y-1/2 text-2xl p-2 text-white bg-black/30 hover:bg-black/50"/>
    <UButton @click="nextSlide"  icon="i-heroicons-chevron-right"  class="absolute right-0 top-1/2 transform -translate-y-1/2 text-2xl p-2 text-white bg-black/30 hover:bg-black/50"/>
  </div>
  </div>
  
</template>


<script lang="ts" setup>
import { ref, computed, onMounted } from 'vue';
import { useBlogStore } from '~/stores/blogs-store';

const searchQuery = ref('');
const blogStore = useBlogStore()


const filteredBlogs = computed(() => {
  if (!blogStore.blogs) return [];
  return blogStore.blogs
    .filter(blogs => {
      return (
        blogs.blogName.toLowerCase().includes(searchQuery.value.toLowerCase()) ||
        blogs.blogStatus.toLowerCase().includes(searchQuery.value.toLowerCase())
      );
    })
    .reverse();
});

onMounted(async () => {
  await blogStore.fetchBlogs();
});

// Active index to control the current slide
const activeIndex = ref(0);

const totalItems = computed(() => filteredBlogs.value.length);
const itemsPerPage = 1; 
const totalPages = computed(() => Math.ceil(totalItems.value / itemsPerPage));

// Move to the next slide
const nextSlide = () => {
  if (activeIndex.value < totalItems.value - 1) {
    activeIndex.value++;
  } else {
    activeIndex.value = 0; // Reset to the first slide if at the end
  }
};

// Move to the previous slide
const prevSlide = () => {
  if (activeIndex.value > 0) {
    activeIndex.value--;
  } else {
    activeIndex.value = totalItems.value - 1; // Go to the last slide if at the beginning
  }
};

const title = ref({
  title: "Latest Products",
  subtitle:
  "Get started - if you own or manage a House, an Apartment or any rental property you can use Leazi to easily and efficiently manage your property(ies) affordably."
});
</script>


<style scoped>
.carousel-container {
  max-width: 1200px;
  margin: auto;
  position: relative;
  width: 100%;
}

.carousel-wrapper {
  display: flex;
}

.carousel-item {
  flex-shrink: 0;
}

.carousel-content {
  background-color: white;
  padding: 16px;
}

button {
  background-color: rgba(0, 0, 0, 0.5);
  border: none;
  color: white;
  padding: 10px;
  cursor: pointer;
  position: absolute;
}

button:hover {
  background-color: rgba(0, 0, 0, 0.7);
}
</style>