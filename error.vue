<template>
  <div class="mt-56">
    <div class="flex items-center justify-center space-x-28">
      <div class="flex flex-col space-y-2 text-center">
        <p class="text-6xl font-bold">{{ error.statusCode }}</p>
        <p class="text-4xl font-bold">{{ error.message }}</p>
        <button class="p-3 text-white bg-purple-600 rounded-lg" @click="handleError">Clear errors</button>
      </div>
      <img src="./assets/img/404-error.png" class="w-64" alt="">
    </div>
  </div>
</template>

<script setup>
defineProps(["error"]);
const handleError = () => clearError({ redirect: "/" });
</script>

<style lang="scss" scoped></style>
