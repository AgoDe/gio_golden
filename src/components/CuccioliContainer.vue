<template>
    <div class="cuccioli">

        <div class="descrizione">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam aspernatur vero alias repudiandae nisi voluptate impedit hic, quaerat, autem distinctio officia a facere. Provident debitis blanditiis libero nostrum illum saepe.
        </div>


        <div class="slider container">
            <div class="row">

                <div class="col-1"
                @click="prevImage()"
                >
                    <i class="icon-chevron-left"></i>
                </div>
                <div class="col-10 img">
                    <img class="col-10" :src="cuccioli[this.activeIndex]" alt="foto_cane">
                    <div class="dot-line">
                        <i 
                        class="icon-circle"
                        :class="activeDot(index)"
                        v-for="(item, index) in cuccioli"
                        :key="index"
                        @click="clickDot(index)"
                        >
                        </i>
                    </div>
                </div>

                <div class="col-1"
                @click="nextImage()"
                >
                    <i class="icon-chevron-right col-1"></i>
                </div>
                
            </div>
        </div>

    </div>
</template>

<script>
export default {
    data(){
       return{
           cuccioli: [
               'https://via.placeholder.com/800x500',
               'https://via.placeholder.com/600x400',
               'https://via.placeholder.com/900x700',
               'https://via.placeholder.com/800x500',
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
                this.activeIndex = this.cuccioli.length -1
            } else {
                this.activeIndex--
            }
        },
        nextImage: function() {
        
            if(this.activeIndex >= this.cuccioli.length -1) {
                this.activeIndex = 0
            } else {
                this.activeIndex++
            } 
        },
        autoplay: function() {
            setInterval(() => {
                if(this.activeIndex >= this.cuccioli.length -1) {
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
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');
@import '/src/styles/main.scss';
@import '/src/styles/slider.scss';
   
   .img {
       border-radius: 25px;
   }
</style>

