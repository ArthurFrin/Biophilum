<script setup lang="ts">
import HeaderTitle from './components/Header.vue'
import NavBar from './components/NavBar.vue'
import WhoIAm from './components/WhoIAm.vue';
import FloraAndFauna from './components/FloraAndFauna.vue';
import WeatArea from './components/WeatArea.vue';
import Watershed from './components/Watershed.vue';
import CateringManagement from './components/CateringManagement.vue';
import FooterContact from './components/footerContact.vue';
import News from './components/News.vue';
</script>

<template>
  <header>
    <HeaderTitle />
  </header>
  <NavBar />
  <main>
    <News />
    <WhoIAm />
    <FloraAndFauna />
    <WeatArea />
    <Watershed />
    <CateringManagement />
    <FooterContact />
    
  </main>

  
</template>

