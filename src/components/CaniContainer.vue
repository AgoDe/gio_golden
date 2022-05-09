<template>
    <div class="nostri-cani">

        <div class="descrizione">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam aspernatur vero alias repudiandae nisi voluptate impedit hic, quaerat, autem distinctio officia a facere. Provident debitis blanditiis libero nostrum illum saepe.
        </div>

       <image-slider
       :imagesArray="cani"
       :showInfo="true"
       />
    </div>
</template>

<script>
import ImageSlider from './ImageSlider.vue'
export default {
  components: { 
      ImageSlider
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
       }
   }, // end of data
  
    
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');
    .nostri-cani {

    }
</style>