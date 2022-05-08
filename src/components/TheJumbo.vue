<template>
  <div class="jumbotron">

      <!-- <img src="https://via.placeholder.com/2000x600" alt="placeholder"> -->
        <div class="container jumbo">
            <div class="row">
                <img class="logo" src="/images/primario.png" alt="logo">
            </div>
        </div>
  </div>
</template>

<script>
import anime from 'animejs/lib/anime.es.js';
export default {
    mounted() {
        //  anime({
        //     targets: ['.enter', '.home'],
        //     translateY: '-100%',
        //     easing: 'steps(8)',
        //     duration: 1500,
        //     });

        anime({

            targets: '.logo',
            // scale: [5,1],
            translateX: [-200, 800],
            opacity: [0.1,1],
            easing:'spring(2, 200, 20, 0)',
            // easing: "easeOutCirc",
            duration: 6000,
        })
    }

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