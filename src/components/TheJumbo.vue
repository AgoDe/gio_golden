<template>
  <div class="jumbotron">

      <!-- <img src="https://via.placeholder.com/2000x600" alt="placeholder"> -->
        <div class="container">
            <div class="row">
                <img src="/images/primario.png" alt="logo">
            </div>
        </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';

    .jumbotron {
       background: url('https://via.placeholder.com/2000x600') center center;
       height: 600px;
       border-bottom: $lineWeight $orange solid;

       .row {

           position: relative;

           img {
               width: 400px;
               position: relative;
               top: 485px;
           }
       }
    }
</style>