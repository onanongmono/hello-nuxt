<template>
  <div class="container m-auto mt-5">
    <p class="text-xl font-bold text-center text-[#77bcf1]">Home</p>
    <p>
      Page visits: {{ data }}
    </p>
    <button p-3 text-white bg-purple-600 rounded-lg><NuxtLink to="/fetch">Fetch</NuxtLink></button>
    <button p-3 text-white bg-purple-600 rounded-lg ml-9><NuxtLink to="/data">AsyncData</NuxtLink></button>
    <button p-3 text-white bg-purple-600 rounded-lg ml-9><NuxtLink to="/mountain">mou</NuxtLink></button>

  </div>
</template>

<script setup lang="ts">
// const { data } = await useAsyncData('count', () => $fetch('/api/count'))
const { data } = await useFetch('/api/count');
definePageMeta({
  layout: "default",
  pageTransition: {
    name: "rotate"
  },
});
</script>
