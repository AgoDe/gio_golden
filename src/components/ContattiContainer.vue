<template>
    <div class="contatti container">
        <div class="row">
            <!-- info contatti -->
            <div class="col-12 col-lg-6 info-container">
                <div class="subtitle">
                    <h4>I nostri contatti</h4>
                </div>
                <div class="info-box">
   
                    <a href="">
                       <i class="icon-mobile"></i>
                       <span>348 8879376</span>
                    </a>

                    <a href="" class="mt-3">
                       <i class="icon-at"></i>
                       <span>info@giogolden.it</span>
                    </a>
                    <a href="" class="mt-3">
                       <i class="icon-location"></i>
                       <span>strada Marscianese, 5 - 06132, Perugia</span>
                    </a>
                </div>

                
                <div class="social-title">
                    Vieni a trovarci nelle nostre pagine social!
                </div>
                <div class="social-box">
                    <a href="https://it-it.facebook.com/giogoldenumbria/" class="facebook">
                       <i class="icon-facebook"></i>
                    </a>
                    <a href="https://www.instagram.com/giogoldenumbria/" class="instagram">
                       <i class="icon-instagram"></i>
                    </a>
                    <a href="https://www.tiktok.com/@giogoldenumbria" class="tiktok">
                       <i class="icon-tiktok"></i>
                    </a>
                </div>
            </div>
            <!-- end of info contatti -->

            <!-- form contatto -->
            <div class="col-12 col-lg-6 form-container">
                <div class="subtitle">
                    <h4>Contattaci!</h4>
                    <h6>compila il form e verrari ricontattato al più presto</h6>
                </div>

                <form-contatti/>
            </div>
            <!-- end of form contatto -->
        </div>
    </div>
</template>

<script>
import FormContatti from './FormContatti.vue'
export default {
    components: { 
        FormContatti
    },
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');
    .contatti {

        .row {

            .subtitle {
                height: 100px;

                h4, h6 {
                       text-align: center;
                       color: $orange;
               }
            }
            .info-container{
                .info-box {
                    display: flex;
                    flex-direction: column;
                    align-items: center;

                    a {
                        
                        width: 80%;
                        height: 50px;
                        border: 2px $orange solid;
                        border-radius:25px;
                        color: $yellow;
                        text-decoration: none;
                        font-size: 18px;

                        i{
                            width: 46px;
                            height: 46px;
                            line-height: 46px;
                            border-radius: 50%;
                            background: $yellow;
                            text-align: center;
                            margin-right:15px ;
                            color: white;
                        }
                    }
                }
                .social-title {
                     margin: 40px 0 15px;
                     color: $orange;
                     font-size: 30px;
                     text-align: center;
                }
                .social-box {
                   
                    display: flex;
                    justify-content: space-around;

                    a {
                        font-size: 30px;
                        width: 60px;
                        height: 60px;
                        line-height: 60px;
                        text-align: center;
                        border-radius: 50%;
                        color: white;
                        position: relative;
                        transition: 0.3s;
                        opacity: 0.9;

                        &:hover  {
                           font-size: 33px;
                           opacity: 1;
                        }
                        &.instagram {
                            background: linear-gradient(167deg, rgba(81,91,212,1) 0%, rgba(129,52,175,1) 35%, rgba(221,42,123,1) 100%);
                            transition: 0.3s;
                        }
                        &.facebook {
                            background-color: #3b5998;
                        }
                        &.tiktok {
                            background-color: #EE1D52;
                        }

                    }
                }
            }

        }
    }
</style>