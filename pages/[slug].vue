<script setup lang="ts">
const route = useRoute()
console.log(route.params.slug)
</script>

<template>
  <h2>strona dynamiczna</h2>
  <h1>{{ $route.params.slug }}</h1>
</template>

<style scoped>

</style>