<script setup lang="ts"></script>
<template>
  <section class="flora-fauna" id="flora-fauna">
    <div class="left">
      <img class="lezard" src="" alt="" />
    </div>
    <div class="right">
      <h2 class="title">Expertise « faune, flore, habitats</h2>
      <div class="div1">
        Biophilum vous propose une expertise « faune, flore, milieux » de qualité permettant
        ’évaluer les écosystèmes afin d’en définir les enjeux de préservation, de restauration et de
        gestion.
      </div>
      <div class="div2">
        Un pré-diagnostic, tout au long de l’année à travers l’évaluation des potentialités
        d’accueil de la faune, de la flore et des habitats. Ce pré-diagnostic permet de mieux cibler
        les inventaires ultérieurs et d’engager une première approche de l’état de conservation et
        du fonctionnement de ces écosystèmes (fonctionnement hydrologique, ...).
      </div>
      <h4 class="h2">
        Des expertises faunes flores habitats, ciblées au regard des potentialités du site et de la
        phénologie des espèces.
      </h4>
      <ul>
        <li>Inventaire botanique et caractérisation des milieux (analyse phytosociologique)</li>
        <li>Inventaire des reptiles et des batraciens</li>
        <li>Inventaire des mammifères</li>
        <li>
          Inventaire des insectes : orthoptères, odonates, lépidoptères, coléoptères
          saproxilophages
        </li>
      </ul>
      <div class="div3">
        Ces expertises se font en partenariat avec d’autres experts en fonction des compétences
        requises. Biophilum est à votre disposition pour répondre à vos besoins et vos questions.
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.flora-fauna {
  display: flex;
  padding: 40px 5% 0 0;
  justify-content: space-around;
  background-color: #008037;
  color: #fff;

  .left {
    display: flex;
    align-items: flex-end;
    width: 50%;

    .lezard {
      width: 800px;
      margin-right: 25px;
      position: relative;
      right: 100px;
    }
  }

  .right {
    max-width: 770px;
    .div1 {
      margin: 25px 0;
    }
    .div2 {
      margin: 0 0 25px;
    }

    .h2 {
      margin: 0 0 10px;
    }
    .div3 {
      margin: 25px 0 0;
    }
  }
}
</style>
