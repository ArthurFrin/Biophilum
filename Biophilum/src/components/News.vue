<script setup lang="ts">
</script>
<template>
  <section class="news" id="news">
    <div class="right mobile">
      <h3 class="title">Mars-Juin 2024 : Évaluation de l’impact des travaux du LIFE Sallina sur les prés salés des
        marais salants de Guérande et du Mès.</h3>
      <p>L’objectif de l’étude est d’évaluer l’impact des travaux (débroussaillage ou bûcheronnage de
        fourrés de ligneux, arrachage de Baccharis halimifolia, pâturage ovin, …) réalisés dans le cadre du LIFE Sallina sur les prés salés atlantiques (code UE : 1330) au sein de 19 sites pilotes.
      </p>
      <p1>La zone d’étude correspond aux linéaires de talus des sites restaurés sur la commune de Pénestin, sur le Bassin de Guérande (communes de Guérande, du Pouliguen et de la Turballe) et sur le Bassin du Mès (communes de Saint-Molf et de Mesquer-Quimiac).
      </p1>
      <p1>L’étude porte sur les prés salés atlantiques du Glauco-Puccinellietalia maritimae (code 1330), ces habitats regroupent l’ensemble des végétations pérennes des prés salés atlantiques, se développant au niveau du schorre.
      </p1>
    </div>
    <div class="pictures desk">
      <figure>
        <img draggable="false" src="../assets/img/181talus-interrieur2.webp" alt="" />
        <figcaption>Habitat des prés salés su haut schorre à l’intérieur des bassins</figcaption>
      </figure>
      <figure>
        <img draggable="false" src="../assets/img/1330-4(2).webp" alt="" />
        <figcaption>Habitat des prés salés du contact haut schorre/dune</figcaption>
      </figure> 
      
    </div>
  </section>
</template>

<style lang="scss" scoped>
.news {
display: flex;
padding: 80px 5% 40px 0;
justify-content: flex-end;
background-color: #008037;
color: #fff;
  
  .right {
    order: 2;
    margin-bottom: 50px;
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    width: 40%;
    
    p {
      margin: 15px 0;
    }

    p1 {
      margin:5px 0;
    }

    .green {
      color: #008037;
    }
    }

.pictures {
  display: flex;
  flex-direction:column;
  align-items: flex-start;
  justify-content:flex-start;
  width: 52%;
  position: relative;

  figure{
    display: flex; /* Disposition en ligne pour aligner image et légende */
    align-items:center; /* Aligne verticalement l'image et la légende */


    img {
      max-width: 400px; /* Taille maximale pour les rendre plus petites */
      margin-bottom: 50px; /* Espace entre les images vertical*/
      border-radius: 50px;
      position: relative;
    }
    
    figcaption {
      margin-top: -50px;
      color: #fff;
    }
  }
  figure:nth-child(1){
    flex-direction: row;
    transform: translate(-70px, 0px);
    figcaption {
      margin-left: 20px; /* Ajoute de l'espace entre l'image et la légende */
    }
  }
  figure:nth-child(2){
    flex-direction: row-reverse;
    transform: translate(-40px, 0px);
    figcaption {
      margin-right:20px; /* Ajoute de l'espace entre l'image et la légende */
    }
  }

}
}
  
  @media screen and (max-width: 1200px) {
    .desk {
      display: none !important;
    }

    .mobile {
      width: 100% !important;
      padding: 5%;
    }


  }
</style>