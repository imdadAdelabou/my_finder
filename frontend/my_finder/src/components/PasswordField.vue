<template>
    <div class="passwd">
        <input :type="type" v-model="v$.password.$model" :placeholder="placeHolder" @change='$emit("getPassword", $event.target.value)'  />
        <img  :src="imgEyes" class="p-viewer" @click="setTypeValue(!eyesClose)"/>
    </div>
</template>

<script>
import useVuelidate from '@vuelidate/core';
import {required} from '@vuelidate/validators';

export default {
    setup: () => ({ v$: useVuelidate() }),
    name: "PasswordField",
    props: {
        placeHolder: {type: String, required: true},
    },
    data() {
        return {
            password: null,
            eyesClose: true,
            type: "password",
            imgEyes: require("../assets/invisible.png"),
        }
    },
    validations: {
        password: {
            required
        }
    },
    methods: {
        setTypeValue(value) {
            this.type = value;
            if (value) {
                this.type = "password";
                this.imgEyes = require("../assets/invisible.png");
                this.eyesClose = true;
            } else {
                this.type = "text";
                this.imgEyes = require("../assets/eye.png");
                this.eyesClose = false;
            }
        },
    },
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