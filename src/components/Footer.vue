<template>
  <v-footer app>
    <v-col class="text-center">
      <img src="/images/logo-small.png" alt="Logo" height="20" />
      <ul class="footer-list">
      <li>
        <span @click="showTerms('termsholder')" class="clickable">Condições gerais de venda</span>
      </li>
      <li>
        <span @click="showTerms('termsconsumer')">Informação ao consumidor</span>
      </li>
      <li><a>Política de privacidade e cookies</a></li>
      <li><a>Livro de reclamações eletrónico</a></li>
      </ul>
    </v-col>
  </v-footer>
</template>

<script setup>
import { ref } from 'vue';

// Variável de controle do overlay
const dialog = ref(false);

// Função para abrir o overlay
const showTerms = () => {
  dialog.value = !dialog.value;
};
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

.clickable {
  cursor: pointer; /* Torna o cursor uma mãozinha */
  color: white; /* Cor azul como um link */
  text-decoration: underline; /* Sublinhado como um link */
  font-weight: bold;
}

.clickable:hover {
  color: darkblue;
}
</style>
