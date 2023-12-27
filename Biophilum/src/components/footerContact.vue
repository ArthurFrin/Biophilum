<script setup lang="ts">
import cvDownloadLink from '../assets/cv-frin-philippe.pdf'
import { ref, onMounted, computed } from 'vue';

const phoneNumber = ref('0602148950');
const isMobile = ref(false);

const formattedPhoneNumber = computed(() => {
  // Ajoutez le formatage du numéro de téléphone selon vos besoins
  return phoneNumber.value;
});

onMounted(() => {
  // Vérifiez si l'appareil est un appareil mobile lors du montage
  isMobile.value = /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
});
</script>

<template>
  <footer id="contact">
    <div class="left">
      <h3 class="title">Contact</h3>
      <nav>
        <a :href="isMobile ? 'tel:' + phoneNumber : '#'" v-if="phoneNumber">
          Téléphone : <strong>{{ formattedPhoneNumber }}</strong>
        </a>
        <a href="mailto:biophilum@orange.fr">Mail : <strong>biophilum@orange.fr</strong></a>
        <a href="mailto:frin_philippe@orange.fr">ou : <strong>frin_philippe@orange.fr</strong></a>
        <a :href="cvDownloadLink" download="cv_frin_philippe.pdf">CV</a>
      </nav>
      <div>Adresse postale : 124 rue de Belphaget 44150 Saint Géréon</div>
    </div>
    <div class="right desk">
      <img class="desk" src="../assets/img/Biophilum_white.png" alt="" />
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  display: flex;
  justify-content: space-between;
  background-color: #1d1d1d;
  color: #fff;
  padding: 0 5%;
  width: 100%;

  a {
    color: #fff;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }

  nav {
    display: flex;
    flex-direction: column;
    margin-bottom: 5px;
  }

  .left {
    margin: 40px 0 20px;
  }

  .right {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    img {
      width: 400px;
    }
  }
}
@media screen and (max-width: 1200px) {
  .desk {
    display: none !important;
  }
}
</style>
