<template>
  <div>
    <nuxt-content :document="article" />
  </div>
</template>

<script>
export default {
  async asyncData({ params, $content }) {
    const article = await $content('blog', params.id).fetch()

    return {
      article,
    }
  },
}
</script>

<style scoped>
.nuxt-content h1 {
  @apply font-medium;
}
</style>