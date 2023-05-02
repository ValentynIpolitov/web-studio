<template>
  <Header />

  <RouterView />

  <Footer />
</template>

<script setup>
import { RouterView } from 'vue-router'
import Header from './shared/Header.vue'
import Footer from './shared/Footer.vue'
</script>

<style scoped>

</style>
