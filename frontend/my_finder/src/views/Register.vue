<template>
    <div class="register">
        <HeadComponent :isLogin="isLogin" route="/login"></HeadComponent>
        <div class="main">
            <input type="text" placeholder="Créer un nom d'utilisateur" />
            <div class="spacerBtw"></div>
            <input type="text" placeholder="Numéro de téléphone" />
            <div class="spacerBtw"></div>
            <PasswordField placeHolder="Mots de passe"></PasswordField>
            <div class="spacerBtw"></div>
            <PasswordField placeHolder="Confirmez votre mots de passe"></PasswordField>
            <div class="spaceBtn"></div>
            <button class="btn" @click="register()" :class="{btnDisabled:  isLoading}">
                <SpinnerBar v-if="isLoading"></SpinnerBar>
                <span v-else>S'inscrire</span>
           </button>
           <BottomComponent></BottomComponent>
        </div>
    </div>
</template>

<style scoped>

    .spacerBtw {
        margin-bottom: 18px;
    }

    .spaceBtn {
        margin-top: 28px;
    }
     .register {
         padding: 0 20px 0 20px;
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
import HeadComponent from '../components/HeadComponent.vue';
import PasswordField from "../components/PasswordField";
import SpinnerBar from "../components/SpinnerBar";
import BottomComponent from "../components/BottomComponent";

export default {
    name: "Register",
    components: {
        HeadComponent,
        PasswordField,
        SpinnerBar,
        BottomComponent
    },
    data() {
        return {
            isLogin: false,
            isLoading: false,
        }
    },
    methods: {
        register() {
            this.isLoading = true;
            console.log("Currently register");
            setTimeout(() => {
                this.isLoading = false;
            }, 2000);
        }
    },
}
</script>
