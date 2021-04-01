<template>
  <div id="blog">
    <ol>
      <li v-for="article of articles" :key="article.slug" class="mb-2">
        <span class="font-font-light text-gray-400 mr-3">
          {{ parseDate(article.createdAt) }}
        </span>
        <nuxt-link class="font-medium" :to="article.path">
          {{ article.title }}
        </nuxt-link>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articles = await $content('blog').fetch()

    return {
      articles,
    }
  },

  methods: {
    parseDate(str) {
      const date = new Date(str)

      return Intl.DateTimeFormat('en-CO', {
        day: 'numeric',
        year: 'numeric',
        month: 'short',
      }).format(date)
    },
  },
}
</script>