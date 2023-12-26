<script setup lang="ts">
import cvDownloadLink from '../assets/cv-frin-philippe.pdf';

</script>

<template>
    <footer id="contact">
        <div class="left">
            <h3 class="title">Contact</h3>
            <nav>
                <a href="tel+0602148950">téléphone : <strong>06 02 14 89 50</strong></a>
                <a href="mailto:biophilum@orange.fr">mail : <strong>biophilum@orange.fr</strong></a>
                <a href="mailto:frin_philippe@orange.fr">ou : <strong>frin_philippe@orange.fr</strong></a>
                <a :href="cvDownloadLink" download="cv_frin_philippe.pdf" >CV</a>
            </nav>
            <div>Adresse postale : 124 rue de Belphaget 44150 Saint Géréon</div>
        </div>
        <div class="right">
            <img src="../assets/img/Biophilum_white.png" alt="">

        </div>
    </footer>
    
</template>

<style lang="scss" scoped>
    footer {
        display: flex;
        justify-content: space-between;
        background-color: #1D1D1D;
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
</style>


