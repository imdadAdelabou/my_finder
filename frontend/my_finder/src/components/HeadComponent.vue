<template>
    <div class="head">
        <div class="cHeader">
            <p>MON LOGO</p>
        </div>
        <div class="main">
            <h3 v-if="isLogin" >Se connecter sur</h3>
            <h3 v-else>S'inscrire sur</h3>
            <p class="subTle">My finder est trés facile</p>
            <div class="spacer"></div>
            <p class="rgst">
                <span v-if="isLogin">Si vous n'avez pas de compte, inscrivez-vous</span>
                <span v-else>Si vous avez déjà un compte, connectez-vous</span>
            </p>
            <div class="sRgst">
                <p class="rgst spaceRgst">Vous pouvez</p>
                <router-link :to="route">
                    <button> 
                        <span v-if="isLogin">Inscrivez-vous ici !</span>
                        <span v-else>connectez-vous ici !</span>
                    </button>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>


export default {
   name: "HeadComponent",
   props: {
       isLogin: {type: Boolean, required: true},
       route: {type: String, required: true},
   }
}

</script>

<style scoped>
     .spacer {
        margin-bottom: 25px;
    }
    .spaceRgst {
        margin: 8px 8px 0 0;
    }

    p {
        margin: 0;
    }

    .main {
        margin-top: 35px;
    }

    .main h3 {
        font-family: "Poppins";
        font-weight: 600;
        font-size: 2em;
        margin: 0;
        
    }

    .main .subTle {
        font-family: "Poppins";
        font-weight: 500;
        line-height: 31px;
        font-size: 1.6em;
    }

    .main .rgst {
        font-family: "Poppins";
        font-weight: 400;
        font-size: 1em;
        margin-bottom: 6px;
    }

    .sRgst {
        display: flex;
        margin-bottom: 53px;
    }
    
    .main .sRgst button {
        border: none;
        padding: 8px;
        border-radius: 5px;
        background-color: #4D47C3;
        color: white;
       cursor: pointer;
       transition: opacity 0.5s ease-in-out;
    }

    .main .sRgst button:hover {
        opacity: 0.5;
    }
</style>