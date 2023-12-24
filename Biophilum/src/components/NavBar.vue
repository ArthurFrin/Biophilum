<script setup lang="ts">
import { onMounted, onBeforeUnmount, ref, type Ref } from 'vue';

const sectionActuelle:Ref<string | null> = ref('who-i-am');

const getSectionActuelle = () => {
  const seuilDeDebut = 50;
  const sections = ['who-i-am', 'flora-fauna', 'weat-area', 'watershed', 'catering-management', 'contact' ];

  for (const section of sections) {
    const element = document.getElementById(section);
    if (element) {
      const rect = element.getBoundingClientRect();
      if (rect.top >= -seuilDeDebut && rect.bottom <= window.innerHeight + seuilDeDebut) {
        return section;
      }
    }
  }

  return null;
};

const detecterSectionActuelle = () => {
  const nouvelleSection = getSectionActuelle();
  if (!nouvelleSection) {
    return;
  }
  if (nouvelleSection !== sectionActuelle.value!) {
    sectionActuelle.value = nouvelleSection;
  }
};

onMounted(() => {
  window.addEventListener('scroll', detecterSectionActuelle);
  console.log(sectionActuelle.value);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', detecterSectionActuelle);
  console.log(sectionActuelle.value);
});

const navigateTo = (section: string) => {
  const element = document.getElementById(section);
  if (element) {
    const topOffset = 40;
    const elementTop = element.getBoundingClientRect().top + window.scrollY;
    window.scrollTo({
      top: elementTop - topOffset,
      behavior: 'smooth'
    });
    sectionActuelle.value = section;
  }
};
</script>

<template>
  <nav class="nav">
    <ul class="bar">
      <li :class="{ active: sectionActuelle === 'who-i-am' }"><button @click="navigateTo('who-i-am')" >Qui suis-je?</button></li>
      <li :class="{ active: sectionActuelle === 'flora-fauna' }"><button @click="navigateTo('flora-fauna')">Faune-flore-habitats</button></li>
      <li :class="{ active: sectionActuelle === 'weat-area' }"><button @click="navigateTo('weat-area')">Zones humides</button></li>
      <li :class="{ active: sectionActuelle === 'watershed' }"><button @click="navigateTo('watershed')">Bassin-versant</button></li>
      <li :class="{ active: sectionActuelle === 'catering-management' }"><button @click="navigateTo('catering-management')">Gestion-restauration</button></li>
      <li :class="{ active: sectionActuelle === 'contact' }"><button @click="navigateTo('contact')">Contact {{ sectionActuelle }}</button></li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
.nav {
  position: sticky;
  top: 0;

  .bar {
    display: flex;
    background-color: #1d1d1d;
    color: white;
    justify-content: space-around;
    padding: 10px 0;
    margin: 0; /* Supprimer la marge par défaut sur la liste */

    li {
      list-style: none; // Supprimer les puces de la liste
      position: relative; // Ajout de position relative pour positionner le pseudo-élément

      &::after {
        content: '';
        display: block;
        position: absolute;
        width: 110%;
        height: 2px; /* Hauteur du soulignement */
        background-color: transparent; /* Couleur du soulignement (transparent par défaut) */
        bottom: -5px; /* Ajustez l'espace entre le texte et le soulignement */
        left: 50%; /* Centre le soulignement par rapport au texte */
        transform: translateX(-50%) scaleX(0);
        border-radius: 4px; /* Coins arrondis */
        transition: transform 0.3s ease-in-out; /* Ajout d'une transition pour un effet d'animation */
      }

      &:hover,
      &.active {
        &::after {
          transform-origin: bottom;
          transform: translateX(-50%) scaleX(1);
          background-color: #ffffff; /* Changez la couleur du soulignement en fonction de vos besoins */
        }

        button {
          text-decoration: none; // Supprimer le soulignement par défaut
        }
      }
    }

    button {
      text-decoration: none; // Supprimer le soulignement par défaut des liens
      color: white;
      background-color: transparent;
      border: none;
      font-size: 18px;
      cursor: pointer;

    }
  }
}
</style>

