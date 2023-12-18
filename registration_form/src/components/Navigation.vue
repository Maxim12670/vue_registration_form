<!-- <script setup>
import AuthorizationForm from './AuthorizationForm.vue';
import RegistrationForm from './RegistrationForm.vue';
import { ref } from 'vue';

let isRegistration = ref(true);

function onUpdateValue(event){
    var id = event.target.id;

    if(id == 'logIn'){
        isRegistration.value = !isRegistration;
    }
    else{
        isRegistration.value = true;
    }

    console.log(isRegistration.value);
}
</script> -->

<script>
import RegistrationForm from './RegistrationForm.vue';
import AuthorizationForm from './AuthorizationForm.vue';

export default{
    components: {
        RegistrationForm,
        AuthorizationForm
    },
    data(){
        return{
            isRegistration: true
        }
    },
    methods: {
        onUpdateValue(event){
            var id = event.target.id;

            if(id === 'logIn'){
                this.isRegistration = false;
            }
            else{
                this.isRegistration = true;
            }
            console.log(this.isRegistration)
        }
    }
}
</script>

<template>
    <div class="navigation">
        <button class="navigation__btn" id="singUp" @click="onUpdateValue">Sing Up</button>
        <button class="navigation__btn" id="logIn" @click="onUpdateValue">Log In</button>
    </div>

    <RegistrationForm v-if="isRegistration"/>
    <AuthorizationForm v-else/>
    
</template>

<style scoped lang="sass">
    @import '../assets/fonts.css'
    .navigation
        display: flex
        justify-content: space-between
        width: 100%
        border: none
        &__btn
            width: 174px
            height: 46px
            border-radius: 23px
            border: 1px solid #23EAC6
            background: rgba(217, 217, 217, 0.20)
            color: #23EAC6
            font-family: "Roboto", sans-serif
            font-size: 15px
            font-weight: 400
            &:focus
                background-color: white
</style>
