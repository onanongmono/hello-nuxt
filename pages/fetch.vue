<template>
  <div class="container m-auto mt-5">
    <p class="text-xl font-bold text-center text-[#77bcf1]">useFetch</p>

    <button p-3 text-white bg-purple-600 rounded-lg @click="$router.back()">
      back
    </button>

    <div mb-2 v-for="mountain in mountains" :key="mountain.title">
      <div>title: {{ mountain.title }}</div>
      <div>height: {{ mountain.height }}</div>
    </div>
  </div>
</template>

<script setup>
// const { data } = await useAsyncData('count', () => $fetch('/api/count'))

const { data: mountains } = await useFetch("https://api.nuxtjs.dev/mountains");
</script>
