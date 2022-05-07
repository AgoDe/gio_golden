<template>
    <footer>

        <div class="container">
            <div class="row">

                <!-- info -->
                <div class="col-12 col-lg-6 info">
                    <img src="/images/Negativo_B.png" alt="logo">
                </div>

                <!-- loghi certificati -->
                <div class="col-12 col-lg-6 loghi">
                    <img src="/images/logo_fci.png" alt="logo_fci">
                    <img src="/images/logo-enci.png" alt="logo_enci">
                    <img src="/images/logo-kennel.png" alt="logo_kennel">
                </div>
            </div>
        </div>

        <!-- logo ADF -->
        <div class="adf">
            <span>Made by</span>
            <img src="/images/logo-square-bw.png" alt="logo-adf">
        </div>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';

footer {
    background: $yellow;

    .container {

        padding: 30px 0;
        .row {

            .info {
                img {
                    height: 60px;
                }
            }

            .loghi {
                display: flex;
                justify-content: space-around;

                img {
                    width: 100px;
                }
            }
        } // end of row
    } // end of container

    
    .adf {
        background: $orange;
        text-align: center;
        

        img {
            height: 50px;
        }
    }
}

</style>