<script setup lang="ts">
const showItem = ref(false)
const buttonText = computed(() => showItem.value ? 'Ukryj telefon' : 'Pokaż telefon')
</script>

<template>
  <h2>strona statyczna</h2>
  <h1>Strona kontakt</h1>

  <button @click="showItem = !showItem">{{buttonText}}</button>
  <br>
  <span v-if="showItem">777 777 777</span>
  <br>
  <span v-show="showItem">888 888 888</span>
<!--  <span v-else>*** *** ***</span>-->

</template>

<style scoped>

</style>