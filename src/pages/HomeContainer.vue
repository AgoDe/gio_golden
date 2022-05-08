<template>
    
    <div class="home-container">
        <the-navbar/>
    
        <the-jumbo/>

        <div class="container">


            <section-title
            :title="'chi siamo'"
            />
            
            <div class="row">
                
            </div>

        </div>

        <the-footer/>
    </div>


</template>

<script>
import TheFooter from '../components/TheFooter.vue'
import TheJumbo from '../components/TheJumbo.vue'
import TheNavbar from '../components/TheNavbar.vue'
import SectionTitle from '../components/SectionTitle.vue'
export default {
    components: {
    TheNavbar,
    TheJumbo,
    TheFooter,
    SectionTitle
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
        height: 600px;
        border-left: $lineWeight $orange solid;
        position: relative;


   }
}

</style>