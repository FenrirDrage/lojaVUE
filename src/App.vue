<template>
  <v-app>
    <NavBar />
    <router-view />
    <Footer />
  </v-app>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'
</script>
