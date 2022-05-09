<template>
    <div class="nostri-cani">

        <div class="descrizione">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam aspernatur vero alias repudiandae nisi voluptate impedit hic, quaerat, autem distinctio officia a facere. Provident debitis blanditiis libero nostrum illum saepe.
        </div>

        <!-- slider -->
        <div class="slider container">
            <div class="row">

                <div class="col-1" @click="prevImage()">
                    <i class="icon-chevron-left"></i>
                </div>

                <div class="col-10 img">
                    <img class="col-10" :src="cani[this.activeIndex].foto" alt="foto_cane">
                    <div class="dot-line">
                        <i 
                        class="icon-circle"
                        :class="activeDot(index)"
                        v-for="(item, index) in cani"
                        :key="index"
                        @click="clickDot(index)"
                        >
                        </i>
                       
                    </div>
                </div>

                <div class="col-1" @click="nextImage()">
                    <i class="icon-chevron-right"></i>
                </div>

                <div class="info col-10 offset-1">
                    <h3>{{cani[this.activeIndex].nome}}</h3>
            
                    <h5>{{cani[this.activeIndex].razza}}</h5>
                    <p>{{cani[this.activeIndex].descrizione}}</p>
        
                </div>
            </div>
        </div>
        <!-- end of slider -->

    </div>
</template>

<script>
export default {
  components: { 
      
   },
   data(){
       return{
           cani: [
               {
                   nome: 'rocco',
                   foto: 'https://via.placeholder.com/800x500',
                   razza: 'americano',
                   descrizione: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam aspernatur vero alias repudiandae nisi '

               },
               {
                   nome: 'matilda',
                   foto: 'https://via.placeholder.com/800x500',
                   razza: 'americano',
                   descrizione: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam aspernatur vero alias repudiandae nisi '

               },
               {
                   nome: 'zoe',
                   foto: 'https://via.placeholder.com/800x500',
                   razza: 'americano',
                   descrizione: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam aspernatur vero alias repudiandae nisi '

               },

           ],       
           activeIndex: 0, 
       }
   }, // end of data
    mounted() {
        this.autoplay()
    }, // end of mounted
    methods: {
        activeDot: function(index) {
            return index == this.activeIndex ? 'active' : ''
        },
        clickDot: function(index) {
            this.activeIndex = index
        },
        prevImage: function() {
            if(this.activeIndex <= 0) {
                this.activeIndex = this.cani.length -1
            } else {
                this.activeIndex--
            }
        },
        nextImage: function() {
        
            if(this.activeIndex >= this.cani.length -1) {
                this.activeIndex = 0
            } else {
                this.activeIndex++
            }
        },
        autoplay: function() {
            setInterval(() => {
                if(this.activeIndex >= this.cani.length -1) {
                this.activeIndex = 0
            } else {
                this.activeIndex++
            }
            }, 4000)
        } 
    }, // end of methods
  
    
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';
@import '/src/styles/slider.scss';
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');
   
</style>