<script setup>
  const { data } = await new Promise((resolve) => {
    setTimeout(() => {
      resolve({ data: 'Hello World' })
    }, 1000)
  })
</script>

<template>
  <h1>
    {{ data }}
  </h1>
</template>