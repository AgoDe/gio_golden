<template>
    <div class="slider container">
        <div class="row">

            <div class="col-1"
            @click="prevImage()"
            >
                <i class="icon-chevron-left"></i>
            </div>
            <div class="col-10 img">
                <img class="col-10" :src="imagesArray[this.activeIndex].foto" alt="foto_cane">
            </div>

            <div class="col-1"
            @click="nextImage()"
            >
                <i class="icon-chevron-right col-1"></i>
            </div>


    
            
            <div class="info col-10 offset-1"
            v-if="showInfo"
            >
                <h3>{{imagesArray[this.activeIndex].nome}}</h3>
        
                <h5>{{imagesArray[this.activeIndex].razza}}</h5>
                <p>{{imagesArray[this.activeIndex].descrizione}}</p>
    
            </div>
        </div>



    </div>
</template>

<script>
export default {
    props: {
        imagesArray: Array,
        showInfo: Boolean,
    },
    data(){
       return{
           activeIndex: 0,
       }
   }, // end of data
     mounted() {

    }, // end of mounted
    methods: {
        prevImage: function() {
            if(this.activeIndex <= 0) {
                this.activeIndex = this.imagesArray.length -1
            } else {
                this.activeIndex--
            }
            console.log('prev:', this.activeIndex)
        },
        nextImage: function() {
        
            if(this.activeIndex >= this.imagesArray.length -1) {
                this.activeIndex = 0
            } else {
                this.activeIndex++
            }
            console.log('next:', this.activeIndex)
        }
    }, // end of methods
    
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');
    .slider {
        // border: solid 4px black;
        margin: 50px 0;
       

        .row {
            flex-wrap: wrap;
            align-items: center;
            height: 100%;
            transition: 0.3s;


            .col-1 {
                cursor: pointer;
                
              
                i {
                    color: $orange;
                    font-size: 60px;
                    position: relative;
                    transition: 0.3s;

                }
                 &:hover i{
                    font-size: 65px;
                    position: relative;
                    color: $yellow;
                    transition: 0.3s;
               }

                &:hover .icon-chevron-left{
                    
                }

            }

            .img {
                border: $lineWeight $orange solid;
                padding: 0;
                border-top-left-radius: 25px;
                border-top-right-radius: 25px;
                overflow: hidden;
                img {
                    width: 100%;
                    object-fit: cover;

                }
            }

            .info {
                background: $orange;
                border-bottom-left-radius: 25px;
                border-bottom-right-radius: 25px;
                padding: 20px;
                color: white;

                h3 {
                    text-transform: uppercase;
                    border-bottom: 1px $yellow solid;
                }
            }

         
        }


    }
</style>