<template>
    <div id="login">
        <div class="cHeader">
            <p>MON LOGO</p>
        </div>
        <div class="main">
            <h3>S'inscrire sur</h3>
            <p class="subTle">My finder est trés facile</p>
            <div class="spacer"></div>
            <p class="rgst">Si vous n'avez pas de compte, inscrivez-vous</p>
            <div class="sRgst">
                <p class="rgst spaceRgst">Vous pouvez</p>
                <button>Inscrivez-vous ici !</button>
            </div>
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
    }
    button {
        border: none;
        padding: 8px;
        border-radius: 5px;
        background-color: #4D47C3;
        color: white;
       
    }

</style>

<script>

export default {
   
}
</script>
