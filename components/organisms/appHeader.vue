<template>
  <header v-if="headerLinks" class="container mx-auto px-4">
    <nav class="flex items-center justify-between bg-white rounded-md shadow-xl p-4 md:px-6">
      <component :blok="headerLinks" :is="headerLinks.component" />
    </nav>
  </header>
</template>

<script>
export default {
  computed: {
    headerLinks () {
      return this.$store.state.layout?.content?.header_links[0]
    }
  }
}
</script>