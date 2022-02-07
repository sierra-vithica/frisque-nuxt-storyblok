<template>
  <div class="container mx-auto px-4">
    <Article
      v-if="story.content.component"
      :key="story.content._uid"
      :blok="story.content"
    />
  </div>
</template>

<script>
export default {
  asyncData(context) {
    const version =
      context.query._storyblok || context.isDev ? 'draft' : 'published'
    const fullSlug =
      context.route.path === '/' || context.route.path === ''
        ? 'home'
        : context.route.path

    // Load the JSON from the API
    return context.app.$storyapi
      .get(`cdn/stories/${fullSlug}`, { version })
      .then((res) => {
        return res.data
      })
      .catch((res) => {
        if (!res.response) {
          // eslint-disable-next-line no-console
          console.error(res)
          context.error({
            statusCode: 404,
            message: 'Failed to receive content from api',
          })
        } else {
          // eslint-disable-next-line no-console
          console.error(res.response.data)
          context.error({
            statusCode: res.response.status,
            message: res.response.data,
          })
        }
      })
  },
  data() {
    return {
      story: { content: {} },
    }
  },

  mounted() {
    this.$storybridge(() => {
      // eslint-disable-next-line no-undef
      const storyblokInstance = new StoryblokBridge({
        customParent: window.location.origin,
      })

      // Listen to Storyblok's Visual Editor event
      storyblokInstance.on(['input', 'published', 'change'], (event) => {
        if (event.action === 'input') {
          if (event.story.id === this.story.id) {
            this.story.content = event.story.content
          }
        } else {
          this.$nuxt.$router.go({
            path: this.$nuxt.$router.currentRoute,
            force: true,
          })
        }
      })
    })
  },
}
</script>
