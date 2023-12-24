<script setup lang="ts">
import HeaderTitle from './components/Header.vue'
import NavBar from './components/NavBar.vue'
import WhoIAm from './components/WhoIAm.vue';
import FloraAndFauna from './components/FloraAndFauna.vue';
import WeatArea from './components/WeatArea.vue';
</script>

<template>
  <header>
    <HeaderTitle />
  </header>
  <NavBar />
  <main>
    <WhoIAm />
    <FloraAndFauna />
    <WeatArea />
  </main>

  
</template>

