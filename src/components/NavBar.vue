<template>
  <v-app-bar app>
    <v-toolbar-title>Voltlider</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn v-if="isMobile" v-for="item in menuItems" :key="item.title" :to="item.link" text>
      {{ item.title }}
    </v-btn>

    <v-menu v-else v-model="menu" offset-y>
      <template v-slot:activator="{ props }">
        <v-btn icon v-bind="props" >
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item v-for="item in menuItems" :key="item.title" :to="item.link">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const menuItems = [
  { title: 'Inicio', link: '/' },
  { title: 'A empresa', link: '/a-empresa' },
  { title: 'Produtos', link: '/produtos' },
  { title: 'Destaques', link: '/destaques' },
  { title: 'Carrinho', link: '/carrinho' },
  { title: 'Contactos', link: '/contactos' },
]

const isMobile = ref(false)
const menu = ref(false)

const checkScreenSize = () => {
  isMobile.value = window.innerWidth > 870
}

onMounted(() => {
  checkScreenSize()
  window.addEventListener('resize', checkScreenSize)
})

onUnmounted(() => {
  window.removeEventListener('resize', checkScreenSize)
})
</script>

<style scoped>
.v-btn {
  margin-right: 16px;
}
</style>
