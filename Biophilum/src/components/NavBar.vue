<script setup lang="ts"></script>
<template>
  <nav class="nav">
    <ul class="bar">
      <li><a href="#">Qui suis-je?</a></li>
      <li><a href="#">Bassin-versant</a></li>
      <li><a href="#">Faune-flore-habitats</a></li>
      <li><a href="#">Zones humides</a></li>
      <li><a href="">Gestion-restauration</a></li>
      <li><a href="">Contact</a></li>
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
    }

    a {
      text-decoration: none; // Supprimer le soulignement par défaut des liens
      color: white;
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

      &:hover {
        &::after {
          transform-origin: bottom;
          transform: translateX(-50%) scaleX(1);
          background-color: #ffffff; /* Changez la couleur du soulignement en fonction de vos besoins */
        }

        text-decoration: none; // Supprimer le soulignement par défaut au survol
      }
    }
  }
}
</style>
