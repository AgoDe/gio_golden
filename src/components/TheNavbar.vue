<template>

    <div class="big-container">
        

        <div class="container">

            <div class="row">

                <a class="navbar-logo col-3" href="#">
                    <img class="" src="/images/primario.png" alt="logo primario">
                </a>


                <nav class="col-9 d-none d-lg-flex">

                    <!-- <i class="icon-bars"></i> -->
                    <a class="" href="#">
                        <p>Chi siamo</p>
                    </a>
                    <a class="" href="#">
                        <p>I nostri cani</p>
                    </a>
                    <a class="" href="#">
                        <p>I nostri cuccioli</p>
                    </a>
                    <a class="" href="#">
                        <p>Contatti</p>
                    </a>

                </nav>


                <div class="mobile col-9 d-lg-none">

                    <i 
                    :class="getClass()"
                    @click="getMobileNav"
                    ></i>

                    <div class="mobile-nav"
                    v-if="nav_visible"
                    >
                        <a class="" href="#">
                            Chi siamo
                        </a>
                        <a class="" href="#">
                            I nostri cani
                        </a>
                        <a class="" href="#">
                            I nostri cuccioli
                        </a>
                        <a class="" href="#">
                            Contatti
                        </a>
                    </div>

                </div>




                

            </div> <!-- end of row -->
        </div> <!-- end of container -->

        
    </div>
</template>

<script>
export default {
    data() {
        return{
            nav_visible: false
        }
    }, // end of data
    mounted() {

    }, // end of mounted
    methods: {
        getMobileNav: function() {
            this.nav_visible = !this.nav_visible
        },
        getClass: function() {
           return this.nav_visible ? 'icon-xmark' : 'icon-bars'
        }
    }, // end of methods
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';


.big-container {

    border-bottom: $lineWeight $orange solid;

    .container {

        padding: 10px;
        .row {
            justify-content: space-between;

            .navbar-logo {
    
                img {
                    height: 60px;
                }
            }

            nav {
                justify-content: flex-end;
                align-items: center;

                a {
                    color: $yellow;
                    text-decoration: none;
                    margin: 0 15px;

                    padding-bottom: 4px;
                    border-bottom: 3px solid transparent;

                    position: relative;
                    display: flex;
                    align-items: center;

                    transition: 0.3s;

                    &:hover {
                        color: $orange;
                        transition: 0.3s;
                    }
                    &:hover p::before{
                        background-color: $orange;
                        color: $orange;
                        transform: scaleX(1);
                        visibility: visible;
                        opacity: 1;
                    }

                   
                    p {
                        text-transform: uppercase;
                        margin: 0;

                        &::before {
                            background-color: rgba(249, 249, 249, 0.4);
                            border-radius: 1px;
                            bottom: -6px;
                            height: 3px;
                            left: 0px;
                            opacity: 1;
                            position: absolute;
                            right: 0px;
                            transform-origin: left center;
                            transform: scaleX(0);
                            transition: all 250ms cubic-bezier(0.25, 0.46, 0.45, 0.94) 0s;
                            visibility: hidden;
                            width: auto;
                            content: '';
                        }
                    }   

                }
            } // end of nav

            .mobile {
                display: flex;
                justify-content: flex-end;
                align-items: center;

                padding-right: 20px;
                font-size: 35px;
                color: $orange;

                position: relative;

                i {
                    cursor: pointer;
                }
                .mobile-nav {
                    position: absolute;
                    right: 0;
                    top: 70px;
                    font-size: 24px;
                    background: $orange;
                    padding: 30px;
                    border-bottom: 5px $yellow solid;

                    display: flex;
                    flex-direction: column;

                    a {
                        margin: 10px 0;
                        color: white;
                        text-decoration: none;
                        border-bottom: 1px solid $yellow;
                        text-transform: uppercase;
                    }
                }

            }
        } // end of row
    } // end of container

}

</style>