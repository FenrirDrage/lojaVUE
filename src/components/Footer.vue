<template>
  <v-footer app>
    <v-col class="text-center">
      <img src="/images/logo-small.png" alt="Logo" height="50" />
      <ul class="footer-list">
      <li><span @click="showTerms('termsholder')">Condições gerais de venda</span></li>
      <li>Informação ao consumidor</li>
      <li><a>Política de privacidade e cookies</a></li>
      <li><a>Livro de reclamações eletrónico</a></li>
      </ul>
    </v-col>
  </v-footer>
</template>

<script setup>
  function showTerms(id) {
    const terms = document.getElementById(id);
    terms.style.display = terms.style.display === 'none' ? 'block' : 'none';
  }
</script>

<style scoped>
.v-btn {
  font-size: 12px;
  margin: 4px 8px;
}
.footer-list {
  list-style-type: none;
  padding: 0;
}
.footer-list li {
  margin:8px 0;
  display: inline;
}
</style>
