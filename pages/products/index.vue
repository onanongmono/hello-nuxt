<template>
  <div class="container m-auto mt-5">
    <!-- <Suspense>
      <template #fallback> Loading...... </template>
      <template #default>
        <div class="grid grid-cols-4 gap-5">
          <div v-for="p in products">
            <ProductCard :product="p" />
          </div>
        </div>
      </template>
    </Suspense> -->
    <div class="grid grid-cols-4 gap-5" >
      <div v-for="p in products">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup>
// const { data: products } = await useFetch(
//   "https://fakestoreapi.com/products"
// );
const { data: products } = await useAsyncData("products", () =>
  $fetch("https://fakestoreapi.com/products")
);
</script>
