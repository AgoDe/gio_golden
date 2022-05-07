<template>
    
    <div class="home-container">
        <the-navbar/>
    
        <the-jumbo/>

        <div class="container">
            
        </div>
    </div>


</template>

<script>
import TheJumbo from '../components/TheJumbo.vue'
import TheNavbar from '../components/TheNavbar.vue'
export default {
    components: { 
        TheNavbar, 
        TheJumbo 
    },
    
}
</script>

<style lang="scss" scoped>

</style>