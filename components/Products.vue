<template>
  <div class="bg-gray-300">
    <div class="carousel-container">
      <Header :item="title" />
      <div>
        <!-- Category Filters as Tabs -->
        <div class="flex border-b-2 bg-gray-700 border-gray-300 rounded-md">

          <div 
            v-for="(category,index) in categories" 
            :key="category.value" 
            class="cursor-pointer transition duration-75  w-full px-4 py-2"
          >

            <div 
              @click="setActiveCategory(category.value)"
              :class="[
                'text-center font-semibold',
                activeCategory === category.value
                  ? 'text-blue-500 py-1 transition-all duration-75 bg-gray-800 rounded-md'
                  : 'text-gray-200 hover:text-blue-400',
              ]"
            >
              {{ category.title }}
            </div>
          </div>
        </div>
      </div>

      <!-- Filtered Items -->
      <div class="grid grid-cols-3 gap-4 p-4">
        <div v-for="item in filteredItems" :key="item.title">
          <UCard>
            <div>
              <img src="../assets/car.jpeg" alt="product image" />
            </div>
            <div class="py-2">
              <h2 class="text-lg font-semibold">{{ item.title }}</h2>
              <span class="font-light">{{ item.star }}</span>
            </div>
            <div class="flex font-light text-gray-500 justify-between items-center border-t border-gray-600">
              <span>auto</span>
              <span>5 persons</span>
              <span>Petrol</span>
            </div>

            <template #footer>
              <div class="flex justify-between">
                <span class="bg-red-500 rounded-l-md text-center py-2 font-bold transition w-1/2">
                  {{ item.price }}
                </span>
                <NuxtLink 
                  class="bg-green-500 rounded-r-md font-bold text-center cursor-pointer hover:bg-gray-700 transition py-2 w-1/2"
                >
                  Rent Now
                </NuxtLink>
              </div>
            </template>
          </UCard>
        </div>
      </div>
    </div>
  </div>
</template>


<script lang="ts" setup>
import { ref, computed } from "vue";

// Header Title
const title = ref({
  title: "Latest Products",
  subtitle:
    "Get started - if you own or manage a House, an Apartment or any rental property you can use Leazi to easily and efficiently manage your property(ies) affordably.",
});

// Categories
const categories = ref([
  { title: "All", value: "all" },
  { title: "Cars", value: "cars" },
  { title: "Bikes", value: "bikes" },
  { title: "Trucks", value: "trucks" },
]);

// Active Category
const activeCategory = ref("all");
const setActiveCategory = (category: string) => {
  activeCategory.value = category;
};

// Items
const items = ref([
  { img: "../assets/car.jpeg", title: "Lamborghini", price: "1000$/day", star: "5.0", category: "cars" },
  { img: "../assets/car.jpeg", title: "Ferrari", price: "600$/day", star: "4.5", category: "cars" },
  { img: "../assets/car.jpeg", title: "Yamaha Bike", price: "200$/day", star: "4.2", category: "bikes" },
  { img: "../assets/car.jpeg", title: "Tesla", price: "500$/day", star: "3.3", category: "cars" },
  { img: "../assets/car.jpeg", title: "Volvo Truck", price: "800$/day", star: "4.8", category: "trucks" },
]);

// Filtered Items Based on Active Category
const filteredItems = computed(() => {
  if (activeCategory.value === "all") {
    return items.value;
  }
  return items.value.filter(item => item.category === activeCategory.value);
});
</script>

<style>
.carousel-container {
  max-width: 1200px;
  margin: auto;
  position: relative;
  width: 100%;
}
</style>
