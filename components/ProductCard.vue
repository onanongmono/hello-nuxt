<template>
  <div class="h-full p-3 text-center rounded-md border border-[#77bcf1 m-auto">
    
      <img :src="product.image" alt="" class="max-h-[120px] m-auto" />
      <p class="m-4 font-bold text-gray-500 truncate">{{ product.title }}</p>
      <NuxtLink :to="`/products/${product.id}`">
        <button class="px-4 py-3 w-full my-4 bg-[#77bcf1] text-sm">View Details</button>
      </NuxtLink>
   
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style scoped></style>
