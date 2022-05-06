<template>
  <div id="app">
  
      <the-navbar/>

  </div>
</template>

<script>
import TheNavbar from './components/TheNavbar.vue'


export default {
  name: 'App',
  components: {
    TheNavbar
    
  }
}
</script>

<style lang="scss">
@import 'bootstrap';
@import '/src/styles/main.scss';

</style>
