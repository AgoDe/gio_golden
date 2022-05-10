<template>
    
    <div class="home-container">
        <the-navbar/>
    
        <the-jumbo/>

        <div class="container">

            <!-- CHI SIAMO -->
            <div id="chi-siamo" class="row">
                <chi-siamo
                class="col-10"
                />
            </div>

            <!-- I NOSTRI CANI -->
            <div id="cani" class="row">
               <cani-container class="col-10"/>
            </div>

            <!-- I NOSTRI CUCCIOLI -->
            <div id="cuccioli" class="row">
                <cuccioli-container class="col-10"/>
            </div>

            <!-- CONTATTI -->
            <div id="contatti">
                <contatti-container class="col-10"/>
            </div>

        </div>

        <the-footer/>
    </div>


</template>

<script>
import TheFooter from '../components/TheFooter.vue'
import TheJumbo from '../components/TheJumbo.vue'
import TheNavbar from '../components/TheNavbar.vue'
import ChiSiamo from '../components/ChiSiamo.vue'
import CaniContainer from '../components/CaniContainer.vue'
import CuccioliContainer from '../components/CuccioliContainer.vue'
import ContattiContainer from '../components/ContattiContainer.vue'
export default {
    components: {
    TheNavbar,
    TheJumbo,
    TheFooter,
    ChiSiamo,
    CaniContainer,
    CuccioliContainer,
    ContattiContainer
},
    
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');

.home-container {
   
    font-family: 'Cabin', sans-serif;
    .container {
        padding: 100px 0;
        // border-left: $lineWeight $orange solid;
        

        .row {
            justify-content: center;
            position: relative;
            margin: 50px 0;
            border: 1px solid black;

        }

   }
}

</style>