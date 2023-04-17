<script setup>
const { data: mountain } = await useFetch(
  'https://api.nuxtjs.dev/mountains/mount-everest'
)
</script>

<template>
  <pre class="overflow-auto text-sm text-left">{{ mountain }}</pre>
</template>
