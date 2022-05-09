<template>
    
    <div class="home-container">
        <the-navbar/>
    
        <the-jumbo/>

        <div class="container">

            <!-- CHI SIAMO -->
           
            <div class="row">
                <h2>chi siamo</h2>
                <chi-siamo
                class="col-10"
                />
            </div>

            <!-- I NOSTRI CANI -->
            <div class="row">
                <h2>i nostri cani</h2>
               <cani-container
               class="col-10"/>
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
export default {
    components: {
    TheNavbar,
    TheJumbo,
    TheFooter,
    ChiSiamo,
    CaniContainer
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
        border-left: $lineWeight $orange solid;
        

        .row {
            justify-content: center;
            position: relative;
            margin: 50px 0;
        }

   }
}

</style>