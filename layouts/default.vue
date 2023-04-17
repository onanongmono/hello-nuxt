<template>
  <div>
    <header>
      <nav class="flex justify-between px-10 py-5 border-b-2 border-[#77bcf1] shadow-lg">
        <h2>Nuxt Mojo</h2>
        <ul class="flex space-x-5">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/products">Products</NuxtLink></li>
          <li><NuxtLink to="/cafe">Cafe</NuxtLink></li>


        </ul>
      </nav>
    </header>

    <div class="container m-auto">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: #77bcf1;
}
</style>