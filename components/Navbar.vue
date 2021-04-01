<template>
  <nav class="navbar justify-center flex-wrap py-6 space-x-3">
    <nuxt-link class="btn" to="/"> Home </nuxt-link>
    <nuxt-link class="btn" to="/blog"> Blog </nuxt-link>
    <nuxt-link class="btn" to="/contact"> Contact </nuxt-link>
  </nav>
</template>

<style scoped>
.btn {
  @apply btn-sm btn-ghost;
}

.btn.nuxt-link-exact-active {
  @apply btn-primary;
}
</style>