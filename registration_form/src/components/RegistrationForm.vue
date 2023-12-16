<script setup>
import { ref } from 'vue';

let person = ref({
    firstName: String,
    lastName: String,
    login: String,
    emil: String,
    password: String,
    photo: null
})

const formElement = document.getElementById('registr');

function createAccount(event){
    event.preventDefault();
    const formData = new FormData(formElement);

}

</script>

<template>
    <div class="content">
        <form id="registr">
            <h2 class="content__title">Create Account</h2>
            <input type="text" name="firstName" class="input" placeholder="First Name" required="required" />
            <input type="text" name="lastName" class="input" placeholder="Last Name" required="required" />
            <input type="text" name="login" class="input" placeholder="Login" required="required" />
            <input type="email" name="email" class="input" placeholder="Email" required="required" />
            <input type="password" name="password" class="input" placeholder="Password" />
            <input type="file" name="photo" class="input input_file" />
            <button class="button" @click="createAccount">create</button>
        </form>
    </div>
</template>

<style scoped lang="sass">
    @import '../assets/fonts.css'
    @import '../assets/styles/blocks/input.sass'
    @import '../assets/styles/blocks/button.sass'
    .content
        color: #FFF
        font-family: "Roboto", sans-serif
        font-size: 20px
        font-weight: 700
        &__title
            margin: 0
            margin-top: 10px
            margin-bottom: 16px
            text-align: center
            font-family: "Roboto", sans-serif
            font-family: 500
        form
            display: flex
            flex-direction: column
</style>
