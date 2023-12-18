<script>
export default{
    name: 'RegistrationForm',
    data(){
        return{
            person: {
                firstName: '',
                lastName: '',
                login: '',
                email: '',
                password: ''
            },
            users: []
        }
    },
    methods: {
        regSubmit(){
            this.users.push({
                'firstName': this.firstName,
                'lastName': this.lastName,
                'login': this.login,
                'email': this.email,
                'password': this.password
            });

            console.log(this.users);
        }
    }
}
</script>

<template>
    <div class="content">
        <form id="registr">
            <h2 class="content__title">Create Account</h2>
            <input v-model="person.firstName" type="text" class="input" placeholder="First Name" />
            <input v-model="person.lastName" type="text" class="input" placeholder="Last Name" />
            <input v-model="person.login" type="text" class="input" placeholder="Login" />
            <input v-model="person.email" type="email" class="input" placeholder="Email" />
            <input v-model="person.password" type="password" class="input" placeholder="Password" />
            <button class="button" @click="regSubmit">create</button>
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
