<template>
    
    <div class="section-title">
        <h2>{{title}}</h2>
        <div>{{title}}</div>
    </div>
</template>

<script>
export default {
   props: {
       title: String,
   },
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');
.section-title {
    position: absolute;
    top: 100px;
    left: -270px;
    width: 500px;
    transform: rotate(-90deg);
    


    h2 {
        color: $orange;
        font-size: 25px;
        z-index: 1001;
        text-transform: uppercase;
    }
    div {
        font-size: 60px;
        text-transform: uppercase;
        position: absolute;
        bottom: 0;
        left: 0;
        opacity: 0.1;
    }
    
}
</style>