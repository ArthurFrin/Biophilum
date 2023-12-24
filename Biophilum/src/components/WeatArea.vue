<script setup lang="ts"></script>

<template>
  <section id="weat-area">
    <div class="left">
      <h3 class="title">Expertise zones humides</h3>
      <p>
        L’identification des zones humides est réalisée sur la base des critères floristiques
        (végétation et habitats) et des critères pédologiques, conformément à l’arrêté du 24 juin
        2008 modifié par l’arrêté du 1er octobre 2009.
      </p>
      <p>
        L’identification des types de sols est basée sur les « Classes d’hydromorphie du Groupe
        d’Etude des Problèmes de Pédologie Appliquée modifié (GEPPA, 1981) », définies par l’arrêté
        du 1er octobre 2009 (cf. schéma ci-dessous).
      </p>
      <p>
        Biophilum bénéficie d’une grande expérience dans l’identification et la caractérisation des
        zones humides. Depuis 2001, j’ai été amené à réaliser des inventaires « zones humides » sur
        de nombreux SAGE : Blavet, Vilaine, Estuaire de la Loire, Grand-lieu,Sèvre Nantaise et Haut
        Val de Sèvre. Ces délimitations et caractérisations ont été menées dans des contextes
        multiples et parfois complexes. Certains sols peuvent prêter à confusion notamment les sols
        d’altération sur schistes parfois classés à tort en zones humides !
      </p>
      <p>
        Une attention particulière doit aussi être portée sur la caractérisation de la végétation
        des plans d’eau. Tous ne sont pas à classer en zones humides, la présence d’herbiers
        aquatiques enracinés est nécessaire pour leur caractérisation en zone humide.
      </p>
      <p>
        Ces milieux particuliers ont des fonctions multiples : régulation hydraulique, épuration,
        biodiversité, …  qu’il convient de caractériser et d’évaluer. Biophilum propose des méthodes
        d’évaluation de ces fonctions à différentes échelles : parcelle, sous-bassin- versant,
        bassin-versant, masse d’eau.
      </p>
      <div>
        Biophilum est à votre disposition <span class="green">pour répondre à vos besoins et vos questions.</span>
      </div>
    </div>
    <div class="right">
      <div class="round-pictures">
        <img src="../assets/img/img1.png" alt="" />
        <img src="../assets/img/img2.png" alt="" />
        <img src="../assets/img/img3.png" alt="" />
      </div>
      <div class="round-pictures">
        <img src="../assets/img/img4.png" alt="" />
        <img src="../assets/img/img5.png" alt="" />
        <img src="../assets/img/img6.png" alt="" />
      </div>
      <img class="schema" src="../assets/img/schema.png" alt="" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  display: flex;
  background-color: #fff;
  width: 100%;
  padding: 85px 0 85px 5%;

  .left {

    display: flex;
    flex-direction: column;
    width: 50%;

    p {
        margin: 15px 0;
    }
    .green {
        color: #008037;
    }
  }
  .right {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 50%;


    .round-pictures {
        display: flex;

      img {
        width: 180px;
        border: solid 3px #008037;
        border-radius: 99999px;
        margin: 3px;
      }
    }
    .schema {
        position: relative;
        margin-top: 100px;
        margin-left: -50px;
        width: 630px;
    }
  }
}
</style>
