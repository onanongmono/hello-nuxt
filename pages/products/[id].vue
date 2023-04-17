<template>
  <div>
    <p>{{ product.title }}</p>
    <!-- <div v-if="pending">Loading....</div>
    <div v-else>
      <p>{{ product.title }}</p>
    </div> -->
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const uri = "https://fakestoreapi.com/products/" + id;

const { data: product } = await useFetch(uri, {key: id});
// const { pending, data: product } = await useLazyFetch(uri, {key: id});
// const { pending, data: product } = await useLazyAsyncData(
//   'products', () => $fetch(uri)
// );

if(!product.value) {
  throw createError({ statusCode: 404, statusMessage: 'Product not found..'})
}
</script>
