<template>
    
    <div class="home-container">

        <the-navbar/>
    
        <the-jumbo/>

        <main class="container">

            <!-- CHI SIAMO -->
            <div id="chi-siamo" class="row">
                 <div class="section-title">
                    <h2>chi siamo</h2>
                    <div>chi siamo</div>
                </div>
                <chi-siamo class="col-10"/>
            </div>

            <!-- I NOSTRI CANI -->
            <div id="cani" class="row">
                 <div class="section-title">
                    <h2>i nostri cani</h2>
                    <div>i nostri cani</div>
                </div>
               <cani-container class="col-10"/>
            </div>

            <!-- I NOSTRI CUCCIOLI -->
            <div id="cuccioli" class="row">
                <div class="section-title">
                    <h2>i nostri cuccioli</h2>
                    <div>i nostri cuccioli</div>
                </div>
                <cuccioli-container class="col-10"/>
            </div>

            <!-- CONTATTI -->
            <div id="contatti" class="row">
                 <div class="section-title">
                    <h2>contatti</h2>
                    <div>contatti</div>
                </div>
                <contatti-container class="col-10"/>
            </div>

        </main>

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

    main {
        padding: 100px 0;
        border-left: $lineWeight $orange solid;
        
        .row {
            justify-content: center;
            position: relative;
            padding-top: 120px;
            // border: 1px solid black;

            .section-title {
                padding-left: 120px;
                position: relative;
                border-bottom: $lineWeight $orange solid;
                margin-bottom: 40px;
                h2 {
                    position: relative;
                    color: $orange;
                    text-transform: uppercase;
                    padding: none;
                    margin: none;
                }
                div {
                    position: absolute;
                    text-transform: uppercase;
                    color: grey;
                    opacity: 0.1;
                    font-size: 60px;
                    left: 20px;
                    bottom: 0;
                }
            }

        }
   }
}

</style>