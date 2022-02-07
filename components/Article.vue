<template>
  <div v-editable="blok" class="p-6 article-block">
    <h1 v-if="blok.title" class="text-5xl bg-purple-400 p-4">
      {{ blok.title }}
    </h1>

    <h2 v-if="blok.intro" class="text-2xl p-3 bg-green-400">
      {{ blok.intro }}
    </h2>

    <div class="flex items-center">

      <NuxtImg
        v-if="blok.image"
        format="webp"
        width="300"
        quality="40"
        provider="storyblok"
        :src="blok.image"
      />

      <p class="text-base" v-html="longText"></p>

    </div>
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true,
    },
  },
  computed: {
    longText() {
      return this.$storyapi.richTextResolver.render(this.blok.long_text)
    },
  },
}
</script>

<style lang="scss">

.text-base {
  @apply bg-red-400;

  p {
    @apply mb-6 p-6;
  }
}

</style>
