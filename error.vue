<template>
  <div class="mt-12 text-center">
    <p class="text-4xl font-bold">{{error.statusCode}}</p>
    <p class="text-4xl font-bold">{{error.message}}</p>

  </div>
</template>

<script setup>
  defineProps(['error'])
</script>

<style lang="scss" scoped>

</style>