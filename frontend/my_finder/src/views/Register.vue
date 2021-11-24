<template>
    <div class="register">
        <HeadComponent :isLogin="isLoading" route="/login"></HeadComponent>
    </div>
</template>

<style scoped>
     .register {
         padding: 0 20px 0 20px;
     }
</style>
   
<script>
import HeadComponent from '../components/HeadComponent.vue';
export default {
    name: "Register",
    components: {HeadComponent,},
    data() {
        return {
            isLoading: false,
        }
    }
}
</script>
