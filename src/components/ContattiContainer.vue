<template>
    <div class="contatti container">
        <div class="row">
            <!-- info contatti -->
            <div class="col-12 col-lg-6 info-container">

                <div class="info-box">

                   
                    <a href="">
                       <i class="icon-mobile"></i>
                       <span>348 8879376</span>
                    </a>

                    <a href="">
                       <i class="icon-at"></i>
                       <span>info@giogolden.it</span>
                    </a>
                    <a href="">
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

            </div>
            <!-- end of form contatto -->
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
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');
    .contatti {

        .row {
            
            .info-container{
                border: 1px solid blue;
                .info-box {
                    display: flex;
                    flex-direction: column;
                    align-items: center;

                    a {
                        box-sizing: content-box;
                        width: 450px;
                        height: 50px;
                        line-height: 50px;
                        border: 3px $orange solid;
                        border-radius:100px;
                        color: $orange;
                        margin: 15px 0;
                        text-decoration: none;
                        font-size: 20px;

                        i{
                            width: 50px;
                            height: 50px;
                            border-radius: 50%;
                            line-height: 50px;
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

            .form-container {
                border: 1px solid red;


            }

        }
    }
</style>