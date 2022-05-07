<template>
    
    <div class="home-container">
        <the-navbar/>
    
        <the-jumbo/>

        <div class="container">

        </div>

        <the-footer/>
    </div>


</template>

<script>
import TheFooter from '../components/TheFooter.vue'
import TheJumbo from '../components/TheJumbo.vue'
import TheNavbar from '../components/TheNavbar.vue'
export default {
    components: { 
        TheNavbar, 
        TheJumbo,
        TheFooter 
    },
    
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';

.home-container {
   

   .container {
       height: 200px;
   }
}

</style>