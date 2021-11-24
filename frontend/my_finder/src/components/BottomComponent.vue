<template>
    <div class="btm">
        <p class="ctn">ou continuer avec</p>
        <div class="options spacer">
            <img src="../assets/Facebook.svg" class="iconSpace"/>
            <img src="../assets/apple.svg" class="iconSpace"/>
            <img src="../assets/google.svg" />
        </div>
    </div>
</template>

<script>

export default {
   name: "BottomComponent",
}
</script>


<style scoped>
    .spacer {
        margin-bottom: 25px;
    }
    
     .options {
        display: flex;
        justify-content: center;
        align-items: center;
    }

     .ctn {
        font-family: 'Poppins';
        font-weight: 500;
        margin: 54px 0 47px 0;
        text-align: center;
        color: #B5B5B5;
        font-size: 1.3em;
    }

    .iconSpace {
        margin-right: 24px;
    }

</style>