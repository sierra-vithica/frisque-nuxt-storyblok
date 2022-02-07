<template>
  <div v-editable="blok" class="container mx-auto px-4">
    <div class="flex justify-between py-16 sm:py-14">
      <div
        class="w-full lg:w-1/2 xl:w-6/12 text-center lg:text-left py-4 sm:p-0"
      >
        <h1
          class="text-4xl xl:text-5xl text-light-onSurfacePrimary dark:text-dark-onSurfacePrimary font-medium tracking-normal leading-tight mb-6"
        >
          {{ blok.headline }}
        </h1>
      </div>
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
}
</script>
