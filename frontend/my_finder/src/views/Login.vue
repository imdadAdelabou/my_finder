<template>
    <div id="login">
        <HeadComponent isLogin=true route="/register"></HeadComponent>
        <div class="main">
           <input type="text" placeholder="Entrez votre pseudo"/>
           <div class="cSpace"></div>
           <PasswordField placeHolder="Entrez votre mots de passe"></PasswordField>
           <div class="clearfix"> </div>
           <p class="fgt">Mots de passe oublié?</p>
           <div class="clearfix"> </div>
           <button class="btn" @click="login()" :class="{btnDisabled:  isLoading}">
           <SpinnerBar v-if="isLoading"></SpinnerBar>
           <span v-else>Se connecter</span></button>
           <BottomComponent></BottomComponent>
        </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap');
    #login {
        padding: 0 20px 0 20px;
    }

    .spacer {
        margin-bottom: 25px;
    }

    .cSpace {
        margin-bottom: 38px;
    }

    .clearfix {
        content: "";
        clear: both;
        display: block;
    }

    p {
        margin: 0;
    }

    .main {
        margin-top: 35px;
    }

    input {
        width: 100%;
        height: 62px;
        border-radius: 8px;
        background-color: #F0EFFF;
        border: none;

    }

    ::placeholder {
        font-family: 'Poppins';
        font-weight: 400;
        color: #A7A3FF;
        font-size: 1.3em;
        padding-left: 23px;
    }

    .p-viewer {
        min-width: 30px;
        height: 30px;
        float: right;
        position: relative;
        z-index: 1;
        cursor: pointer;
        margin-top: -45px;    
    }

    .fgt {
        margin-top: 17px;
        float: right;
        color: #B0B0B0;
        font-family: 'Poppins';
        font-weight: 400;
        font-size: 1.2em;
        margin-bottom: 46px;
    }

    .btn {
        width: 100%;
        height: 59px;
        border: none;
        border-radius: 9px;
        background-color: #4D47C3;
        box-shadow: 0px 4px 61px rgba(77, 71, 195, 0.4);
        color: white;
        font-family: 'Poppins';
        font-weight: 400;
        font-size: 1.6em;
        cursor: pointer;
        transition: opacity 0.5s ease-in-out;
    }

    .btn:hover {
        opacity: 0.9;
    }

    .btnDisabled {
        background-color: grey;
        cursor: not-allowed;
    }

</style>

<script>
import SpinnerBar from '../components/SpinnerBar';
import HeadComponent from '../components/HeadComponent.vue';
import PasswordField from '../components/PasswordField';
import BottomComponent from '../components/BottomComponent';

export default {
    name: "Login",
    data() {
        return {
            isLoading: false,
        };
    },
    methods: {
        login() {
            this.isLoading = true;
            console.log("Currently login");
            setTimeout(() => {
                this.isLoading = false;
            }, 2000);
        },
    },
    components: {
        SpinnerBar,
        HeadComponent,
        PasswordField,
        BottomComponent,
    }
}
</script>
