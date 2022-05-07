<template>
  <div id="app">
  
      <the-navbar/>

      <the-jumbo/>
      
  </div>
</template>

<script>
import TheJumbo from './components/TheJumbo.vue'
import TheNavbar from './components/TheNavbar.vue'


export default {
  name: 'App',
  components: {
    TheNavbar,
    TheJumbo
    
  }
}
</script>

<style lang="scss">
@import 'bootstrap';
@import '/src/styles/main.scss';

</style>
