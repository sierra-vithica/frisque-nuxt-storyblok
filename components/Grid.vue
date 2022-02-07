<template>
  <ul v-editable="blok" class="flex py-8">
    <li v-for="block in blok.columns" :key="block._uid" class="flex-auto px-6">
      <component :is="block.component" :blok="block" />
    </li>
  </ul>
</template>

<script>
export default {
  name: 'GridBlok',
  props: {
    blok: {
      type: Object,
      required: true,
    },
  },
}
</script>
