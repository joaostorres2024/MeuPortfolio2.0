<script setup lang="ts">
import { ref, onMounted } from 'vue';
import cabecalho from './components/cabecalho.vue';
import apresentacao from './components/apresentacao.vue';
import LoadingScreen from './components/loadingscreen.vue';

const loading = ref(true);

const hideLoadingScreen = () => {
  loading.value = false;
};

onMounted(() => {
  setTimeout(hideLoadingScreen, 2000); // Simula o tempo de carregamento
});
</script>

<template>
  <LoadingScreen :visible="loading" />
  <cabecalho></cabecalho>
  <apresentacao></apresentacao>
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
  font-family: 'Poppins';
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
</style>
