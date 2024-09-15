<script setup lang="ts">
import { ref, type Ref } from 'vue'
import IconBurger from './icons/IconBurger.vue'

const currentSection: Ref<string | null> = ref('who-i-am')
const canDetect = ref(true)
let showBurger = ref(false)

const toggleBurger = () => {
  showBurger.value = !showBurger.value
}

const getCurrentSection = (): string | null => {
  if (canDetect.value === false) {
    return null
  }

  const threshold = 50
  const offset = 100
  const sections = [
    'news',
    'who-i-am',
    'flora-fauna',
    'weat-area',
    'watershed',
    'catering-management',
    'contact'
  ]
  const isAtBottom = window.innerHeight + window.scrollY >= document.body.scrollHeight - threshold

  if (isAtBottom) {
    return 'contact'
  }

  for (const section of sections) {
    const element = document.getElementById(section)
    if (element) {
      const rect = element.getBoundingClientRect()
      const isSectionVisible = rect.top <= threshold + offset && rect.bottom >= -threshold + offset

      if (isSectionVisible) {
        return section
      }
    }
  }

  return null
}

const detectCurrentSection = () => {
  const newSection = getCurrentSection()
  if (!newSection) {
    return
  }
  if (newSection !== currentSection.value) {
    currentSection.value = newSection
  }
}
window.addEventListener('scroll', detectCurrentSection)

const scrollTo = (element: HTMLElement, topOffset: number) => {
  return new Promise<void>((resolve) => {
    const elementTop = element.getBoundingClientRect().top + window.scrollY
    window.scrollTo({
      top: elementTop - topOffset,
      behavior: 'smooth'
    })

    const scrollHandler = () => {
      window.removeEventListener('scroll', scrollHandler)
      resolve()
    }

    window.addEventListener('scroll', scrollHandler)
  })
}

const navigateTo = async (section: string) => {
  canDetect.value = false
  currentSection.value = section

  const targetElement = document.getElementById(section)
  if (targetElement) {
    const topOffset = 40
    await scrollTo(targetElement, topOffset)

    canDetect.value = true
  }
}
</script>

<template>
  <nav class="nav">
    <ul class="bar">
      <li :class="{ active: currentSection === 'news' }">
        <button @click="navigateTo('news')">Les actualités</button>
      </li>
      <li :class="{ active: currentSection === 'who-i-am' }">
        <button @click="navigateTo('who-i-am')">Qui suis-je?</button>
      </li>
      <li :class="{ active: currentSection === 'flora-fauna' }">
        <button @click="navigateTo('flora-fauna')">Faune-flore-habitats</button>
      </li>
      <li :class="{ active: currentSection === 'weat-area' }">
        <button @click="navigateTo('weat-area')">Zones humides</button>
      </li>
      <li :class="{ active: currentSection === 'watershed' }">
        <button @click="navigateTo('watershed')">Bassin-versant</button>
      </li>
      <li :class="{ active: currentSection === 'catering-management' }">
        <button @click="navigateTo('catering-management')">Gestion-restauration</button>
      </li>
      <li :class="{ active: currentSection === 'contact' }">
        <button @click="navigateTo('contact')">Contact</button>
      </li>
    </ul>
  </nav>
  <nav :class="{ toogle: showBurger === true }" class="mobile">
    <button @click="toggleBurger()" class="burger">
      <IconBurger class="icon" />
    </button>
    <ul v-if="showBurger" class="bar2">
      <li>
        <button @click="navigateTo('news')">Les actualités</button>
      </li>
      <li>
        <button @click="navigateTo('who-i-am')">Qui suis-je?</button>
      </li>
      <li>
        <button @click="navigateTo('flora-fauna')">Faune-flore-habitats</button>
      </li>
      <li>
        <button @click="navigateTo('weat-area')">Zones humides</button>
      </li>
      <li>
        <button @click="navigateTo('watershed')">Bassin-versant</button>
      </li>
      <li>
        <button @click="navigateTo('catering-management')">Gestion-restauration</button>
      </li>
      <li>
        <button @click="navigateTo('contact')">Contact</button>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
.nav {
  position: sticky;
  top: 0;
  z-index: 100;

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

.mobile {
  display: none;
}

@media screen and (max-width: 800px) {

  .toogle {
    background-color: #1d1d1ded;
    color: #fff;
    fill: #fff;
    padding-bottom: 5px;
    padding-right: 5px;
    border-bottom-right-radius: 20px;
  }
  .nav {
    display: none;
  }

  .mobile {
    display: block;
    position: fixed;
    top: 0;
    padding-top: 5px;
    z-index: 100;

    .bar2 {
      padding: 0;
      li {
        list-style: none; // Supprimer les puces de la liste

        button {
          text-decoration: none; // Supprimer le soulignement par défaut des liens
          color: currentColor;
          background-color: transparent;
          border: none;
          font-size: 18px;
          cursor: pointer;
        }
      }
    }
    .burger {
      width: 40px;
      height: 40px;
      border: none;
      background-color: transparent;
      .icon {
        width: 40px;
        height: 40px;
      }
    }
  }
}
</style>
