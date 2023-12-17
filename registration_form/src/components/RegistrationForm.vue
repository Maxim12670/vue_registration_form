<script>
export default {
    setup() {
        const data = {
            info: {
                firstName: '',
                lastName: '',
                login: '',
                email: '',
                password: '',
                photo: null
            },
            users: [

            ],
        };
    },
    methods: {
        registration: function () {
            this.users.push({
                'firstName': this.info.firstName,
                'lastName': this.info.lastName,
                'login': this.info.login,
                'email': this.info.email,
                'password': this.info.password,
            });

            this.info.firstName = '';
            this.info.lastName = '';
            this.info.login = '';
            this.info.email = '';
            this.info.password = '';

            console.log(data);
        }
    }
}
</script>

<template>
    <div class="content">
        <form id="registr">
            <h2 class="content__title">Create Account</h2>
            <input type="text" v-mpdel="info.firstName" class="input" placeholder="First Name" required="required" />
            <input type="text" v-mpdel="info.lastName" class="input" placeholder="Last Name" required="required" />
            <input type="text" v-mpdel="info.login" class="input" placeholder="Login" required="required" />
            <input type="email" v-mpdel="info.email" class="input" placeholder="Email" required="required" />
            <input type="password" v-mpdel="info.password" class="input" placeholder="Password" />
            <input type="file" v-mpdel="info.email" class="input input_file" />
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
