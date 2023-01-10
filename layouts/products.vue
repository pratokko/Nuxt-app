<template>
  <div>
    <header class="shodow-sm bg-white">
      <nav class="container mx-auto p-4">
        <NuxtLink to="/products">Nuxt-App Merch</NuxtLink>
      </nav>
    </header>
    <!-- this output the page content-->

    <div class="container mx-auto p-4">
      <slot />
    </div>
  </div>

  <footer class="container mx-auto p-4 flex justify-between botder-t-2">
    <ul class="flex gap-4">
      <li><NuxtLink to="/">Home</NuxtLink></li>
      <li><NuxtLink to="/about">About</NuxtLink></li>
      <li><NuxtLink to="/products">Products</NuxtLink></li>
    </ul>
  </footer>

</template>
<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>
