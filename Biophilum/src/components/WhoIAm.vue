<script setup lang="ts">
import cvDownloadLink from '../assets/cv-frin-philippe.pdf';

</script>

<template>
  <section class="section1" id="who-i-am">
    <div class="left">
      <h2 class="title">Qui suis-je ?</h2>
      <div class="flex div-cv">
        <div class="name">Philippe Frin</div>
        <div class="inge">Ingénieur Écologues 
          <a :href="cvDownloadLink" download="cv_frin_philippe.pdf" class="cv-link" >(voir CV)</a>
        </div>
      </div>
      <div class="conseil">
        <strong>Biophilum</strong> est une structure de conseils, d’études et de formations en
        environnement à destination de tous (collectivités territoriales, professionnels,
        associations, collectifs, particuliers, …).
      </div>
      <div class="plaquette">Télécharger <span class="link">la plaquette</span></div>
      <div class="xp">
        L’objectif est d’apporter une <strong>expertise indépendante</strong>, transparente et
        accessible à tous pour permettre des prises de décision en toute connaissance et en toute
        conscience.
      </div>
      <div class="domaine">Domaines d’activités :  milieux naturels – eau – faune -flore</div>
      <ul>
        <li class="li">
          Diagnostics de territoire (inventaires zones humides, pré-diagnostic, cartographie des
          habitats …).
        </li>
        <li class="li">
          Études techniques et élaboration de projets (plans de gestion, aménagement des bassins
          versants, …).
        </li>
        <li class="li">Assistance technique (DCE, projets, chantiers).</li>
        <li class="li">
          Formations « milieux naturels » (zones humides, espèces envahissantes, milieux
          aquatiques, …).
        </li>
      </ul>
      <div class="adapte">
        <strong>Biophylum</strong> s’adapte au mieux à vos contraintes, il suffit d’en discuter !
      </div>
      <div>
        <strong>Biophylum</strong> c’est aussi un projet basé sur le partenariat, pour compléter les
        compétences, l’analyse et les expériences.
      </div>
    </div>
    <div class="right desk">
      <img class="plante1 desk" src="../assets/img/plante1.png" alt="" />
    </div>
  </section>
</template>
<style lang="scss" scoped>
.section1 {
  display: flex;
  padding: 0 5%;
  justify-content: space-between;
  background-color: #fff;
  width: 100%;

  .left {
    margin: 49px 0 32px;
    max-width: 680px;
  }

  .name {
    font-size: 27px;
    font-weight: 700;
    margin-right: 18px;
  }

  .inge {
    margin-top: 7px;
  }
  .cv-link {
    color: green;
  }

  .cv {
    margin-top: 9px;
    padding-left: 25px;
    font-size: 18px;
  }

  .div-cv {
    margin: 32px 0 21px;
  }

  .conseil {
    margin-top: 7px;
  }

  .plaquette {
    margin: 18px 0 30px;
  }

  .xp {
    margin-bottom: 22px;
  }

  .domaine {
    margin-bottom: 11px;
  }

  .li {
    margin-top: 11px;
  }

  .adapte {
    margin: 11px 0 22px;
  }

  .right {
    display: flex;
    align-items: flex-end;
  }
  .plante1 {
    width: 652px;
    height: 912px;
  }
  
}

@media screen and (max-width: 1200px) {
  .desk {
    display: none !important;
  }
}
</style>
