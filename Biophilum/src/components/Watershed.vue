<script setup lang="ts">
</script>
<template>
  <section class="watershed" id="watershed">
    <div class="left desk">
        <img class="desk" src="../assets/img/group1.png" draggable="false" alt="">
    </div>
    <div class="right mobile">
      <h3 class="title">Expertise « bassin versant »</h3>
      <p class="p">
        L’analyse de la structure d’un territoire, à l’échelle d’un bassin versant ou d’une
        exploitation agricole, passe par un relevé fin des éléments du paysage et une compréhension
        des interactions entre ces différents éléments constitutifs. 
      </p>
      <p class="p">
        Cette analyse permet de définir les différentes fonctions potentiels et actives au sein du
        territoire et ainsi déterminer les actions de préservation, de restauration et/ou de
        création à entreprendre afin de tendre vers un meilleur fonctionnement.
      </p>
      <ul class="p">
        <li><strong>Relevé de l’occupation du sol</strong> (habitats naturels et semi-naturels)</li>
        <li>Définition de l’état de conservation des milieux</li>
        <li>
          Définition <strong>des stades d’évolution</strong> des milieux et
          <strong>dynamiques en cours</strong>
        </li>
        <li>
          Caractérisation des flux hydrauliques (ruisseaux, fossés circulants, ruissellements, …)
        </li>
        <li>
          Caractérisation du <strong>maillage des haies</strong> (strates, arbres à cavités, …)
        </li>
        <li>Identification des courts-circuits (talus, ruptures de pente, drainages, … )</li>
        <li>
          Identification <strong>des potentialités d’accueil de la faune et de la flore</strong>
        </li>
        <li>Analyse des conduites agronomiques</li>
      </ul>
      <p class="p">
        <strong>Permettant ainsi de définir et de hiérarchiser les fonctions : </strong>
      </p>
      <ul class="p">
        <li>
          <strong>Hydraulique :</strong> ralentissement des ruissellements, expansion des crues ...
        </li>
        <li><strong>Epuration :</strong> épuration par sédimentation, épuration biologique ...</li>
        <li><strong>Anti-érosive :</strong> talus anti-érosif, boisement sur forte pente …</li>
        <li><strong>Stockage de carbone :</strong> boisements, haies, sol ...</li>
        <li>
          <strong>Biodiversité :</strong> Habitats ou espèces d’intérêts patrimoniales, diversité
          d’habitats, corridors biologiques, réservoirs de biodiversité … 
        </li>
      </ul>
      <p class="p">
        Pour aboutir à la <strong>définition des enjeux</strong> et
        <strong>l’élaboration d’un plan d’actions</strong> concerté avec les acteurs du territoire.
      </p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.watershed {
  display: flex;
  width: 100%;
  background-color: #008037;
  padding: 0 5% 0 0;
  .left {
      width: 50%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin-left: 2%;
    }

    img {
      border-radius: 5px;
      margin: 20px;
      width: 600px;
    }
}

.right {
  color: #fff;
  width: 50%;
  margin-top: 80px;

  .p {
    margin: 15px 0;
  }
}

@media screen and (max-width: 1200px) {
  .desk {
    display: none !important;
  }
  .mobile {
    width: 100% !important;
    padding-left: 5%;
}
}
</style>
