<template>
  <div class="container m-auto mt-5">
    <p class="text-xl font-bold text-center text-purple-500">useAsyncData</p>
    <button p-3 text-white bg-purple-600 rounded-lg @click="$router.back()">black</button>

    <!-- <ul>
      <li v-for="cafe in posts.data" 
        :key="cafe.id" 
        v-text="cafe.company.name+' - '+cafe.location_name"></li>
    </ul> -->
    <div v-for="mountain in data" :key="mountain.title">
      <div>{{ mountain.title }}</div>
      <div>{{ mountain.height }}</div>

    </div>
  </div>
</template>

<script setup>
// const { data } = await useAsyncData('count', () => $fetch('/api/count'))
const { data, pending, error, refresh } = await useAsyncData(
  'mountains',
  () => $fetch('https://api.nuxtjs.dev/mountains')
)

// const page = ref(1)
// const { data: posts } = await useAsyncData(
//   'posts',
//   () => $fetch('https://fakeApi.com/posts', {
//     params: {
//       page: page.value
//     }
//   }), {
//     watch: [page]
//   }
// )


</script>
