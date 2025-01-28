<template>
  <v-footer app>
    <v-col class="text-center">
      <v-btn text :to="'/condicoes-gerais-de-venda'">Condições gerais de venda</v-btn>
      <v-btn text :to="'/informacao-ao-consumidor'">Informação ao consumidor</v-btn>
      <v-btn text :to="'/politica-de-privacidade-e-cookies'">Política de privacidade e cookies</v-btn>
      <v-btn text :to="'/livro-de-reclamacoes-eletronico'">Livro de reclamações eletrónico</v-btn>
    </v-col>
  </v-footer>
</template>

<script setup>
// You can add any necessary script here if needed
</script>

<style scoped>
.v-btn {
  margin: 8px;
}
</style>
