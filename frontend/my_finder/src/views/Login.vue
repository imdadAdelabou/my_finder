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
           <input type="text" placeholder="Entrez votre pseudo"/>
           <div class="cSpace"></div>
           <input type="password" placeholder="Entrez votre mots de passe"/>
           <img src="../assets/invisible.png" class="p-viewer"/>
           <div class="clearfix"> </div>
           <p class="fgt">Mots de passe oublié?</p>
           <div class="clearfix"> </div>
           <button class="btn">S'inscrire</button>
           <p class="ctn">ou continuer avec</p>
           <div class="options spacer"> 
            <img src="../assets/Facebook.svg" class="iconSpace"/>
            <img src="../assets/apple.svg" class="iconSpace"/>
            <img src="../assets/google.svg" />
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

    .cSpace {
        margin-bottom: 38px;
    }

    .iconSpace {
        margin-right: 24px;
    }

    .clearfix {
        content: "";
        clear: both;
        display: block;
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

    .ctn {
        font-family: 'Poppins';
        font-weight: 500;
        margin: 54px 0 47px 0;
        text-align: center;
        color: #B5B5B5;
        font-size: 1.3em;
    }

    .options {
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>

<script>

export default {
   
}
</script>
