<template>
  <div v-editable="blok" class="p-6">
    <component
      :is="block.component"
      v-for="block in blok.body"
      :key="block._uid"
      :blok="block"
    />
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
