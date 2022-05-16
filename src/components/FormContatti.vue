<template>
    <div class="form-contatti">

        
        <div class="box" :class="{'error' : error.nome }">
            <div class="label">Nome</div>
            <input class="cap" type="text" id="nome" placeholder="" v-model="form.nome">
        </div>
        <div class=" error-message" v-if="error.nome">
            Inserisci un nome valido
        </div>
    
        <!-- <div class="box">
            <div class="label">Cognome</div>
            <input class="cap" type="text" id="nome" placeholder="" v-model="form.cognome">
        </div> -->
    
    
        <div class="box mt-3" :class="{'error' : error.email }">
            <div class="label">E-mail</div>
            <input class="" type="e-mail" id="nome" placeholder="" v-model="form.email">
        </div>
        <div class=" error-message" v-if="error.email">
            Inserisci un indirizzo e-mail valido
        </div>

        <div class="box textarea mt-3" :class="{'error' : error.messaggio }">
            <div class="label textarea">Messaggio</div>
            <textarea name="" id="" cols="30" rows="10" v-model="form.messaggio"></textarea>
        </div>
        <div class=" error-message" v-if="error.messaggio">
            Inserisci un messaggio
        </div>
        

        <button
        class="mt-3"
        @click="submit()"
        >invia</button>

    </div>
</template>

<script>

export default {
    data(){
        return{
            form: {
                nome: '',
                email: '',
                messaggio: '',
            },
            error: {
                nome: false,
                email: false,
                messaggio: false,
            }
        }
    },
    methods: {
        validateName: function() {
            if ((this.form.nome == "") || (this.form.nome == "undefined")) {
                // alert("Il campo Nome è obbligatorio.");
                this.error.nome = true
                return false;
            } else {
                this.error.nome = false
                return true
            }
        },
        validateMessage: function() {
            if ((this.form.messaggio == "") || (this.form.messaggio == "undefined")) {
                // alert("Il campo Nome è obbligatorio.");
                this.error.messaggio = true
                return false;
            } else {
                this.error.messaggio = false
                return true
            }
        },
        validateMail: function() {
            
            const email_reg = /^([a-zA-Z0-9_.-])+@(([a-zA-Z0-9-]{2,})+.)+([a-zA-Z0-9]{2,})+$/;
            if (!email_reg.test(this.form.email) || (this.form.email == "") || (this.form.email == "undefined")) {
            // alert("Inserire un indirizzo email corretto.");
            this.error.email = true
            return false;
            } else {
                this.error.email = false
                return true
            }
        },
        submit: function() {
            this.validateName();
            this.validateMail();
            this.validateMessage();
            if(this.validateName() && this.validateMail() && this.validateMessage()) {
                console.log('form validato')
            } else {
                console.log('form non validato')
            }
          
        }

    }
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '/src/styles/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Cabin&display=swap');

.form-contatti {
    display: flex;
    flex-direction: column;
    align-items: center;
    .box {
        position: relative;
        border: 2px $orange solid;
        height: 50px;
        width: 80%;
        border-radius: 25px;
        font-size: 18px;
        display: flex;

        &.textarea {
            height: 300px;
            flex-direction: column;
        }

        .label {
            padding-left: 20px;
            background: $yellow;
            height: 46px;
            line-height: 46px;
            width: 150px;
            border-radius: 23px;
            color: white;

            &.textarea {
                width: 100%;
                border-bottom-left-radius: 0;
                border-bottom-right-radius: 0;
            }


        }
        input {
            border: none;
            padding-left:10px ;
            color: $yellow;
            width: 90%;
            background: transparent;

            &.cap {
                text-transform: capitalize;
            }

            &:focus-visible {
                outline: none;
            }
        }
        textarea {
            border: none;
            border-radius: 25px;
            height: 100%;
            padding:15px ;
            color: $yellow;
             &:focus-visible {
                border: none;
                outline: none;
            }
        }

        &.error {
            border-color: red;
            color:red;
            
        }
    }
    .error-message {
        color: red;
    }

    button {
        width: 80%;
        height: 50px;
        border-radius: 25px;
        background: $yellow;
        border: 2px $orange solid;
        color: white;
        text-transform: uppercase;
    }
}

</style>