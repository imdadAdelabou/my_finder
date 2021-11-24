<template>
    <div class="passwd">
        <input type="password" :placeholder="placeHolder"/>
        <img src="../assets/invisible.png" class="p-viewer"/>
    </div>
</template>

<script>

export default {
    name: "PasswordField",
    props: {
        placeHolder: {type: String, required: true},
    }
}

</script>

<style scoped>
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
</style>