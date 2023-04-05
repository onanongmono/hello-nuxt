<template>
  <div class="container m-auto mt-5">
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <ProductCard :product="p" />
        <!-- <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink> -->
      </div>
    </div>
  </div>
</template>

<script setup>
  const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>
