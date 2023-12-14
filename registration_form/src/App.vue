<script setup></script>

<template>
    <div class="form">
        <div class="form-btn">
            <button class="btn">Sing Up</button>
            <button class="btn">Log In</button>
        </div>
        <div class="form-content">
            <form action="">
                <h2 class="form-content__title">Create Account</h2>
                <input
                    type="text"
                    name="firstName"
                    class="form-content__input"
                    placeholder="First Name"
                    required="required"
                />
                <input
                    type="text"
                    name="lastName"
                    class="form-content__input"
                    placeholder="Last Name"
                    required="required"
                />
                <input
                    type="text"
                    name="login"
                    class="form-content__input"
                    placeholder="Login"
                    required="required"
                />
                <input
                    type="email"
                    name="email"
                    class="form-content__input"
                    placeholder="Email"
                    required="required"
                />
                <input
                    type="password"
                    name="password"
                    class="form-content__input"
                    placeholder="Password"
                />
                <input
                    type="file"
                    name="file"
                    class="form-content__input_file"
                />
                <button class="button">create</button>
            </form>
        </div>
    </div>
</template>

<style scoped lang="sass">
@import 'assets/fonts.css'
.form
    position: absolute
    margin: auto
    top: 0
    right: 0
    bottom: 0
    left: 0
    width: 500px
    height: 512px
    padding: 35px 42px
    border-radius: 5%
    border: 5px solid rgba(255, 255, 255, 0.40)
    box-shadow: 10px -10px 5px 9px rgba(139, 90, 208, 0.2)
    background: #444
    &-btn
        display: flex
        justify-content: space-between
        width: 100%
        border: none

    .btn
        width: 174px
        height: 46px
        border-radius: 23px
        border: 1px solid #23EAC6
        background: rgba(217, 217, 217, 0.20)
        color: #23EAC6
        font-family: "Roboto", sans-serif
        font-size: 15px
        font-weight: 400

    .form-content
        color: #FFF
        font-family: "Roboto", sans-serif
        font-size: 20px
        font-weight: 700
        &__title
            margin: 0
            margin-top: 10px
            margin-bottom: 16px
            text-align: center
            font-family: 500
        form
            display: flex
            flex-direction: column
        &__input
            margin-bottom: 11px
            width: 100%
            height: 36px
            box-sizing: border-box
            padding: 9px 19px
            background: #444
            border-radius: 18px
            border: 1px solid #23eac6
            color: rgba(35, 234, 198, 0.40)
            font-family: "Roboto", sans-serif
            font-size: 15px
            font-weight: 500
            :active
                background-color: #fff
            &_file
                margin-top: 16px

    .button
        width: 326px
        height: 56px
        box-sizing: border-box
        text-align: center
        margin: 0 auto
        margin-top: 40px
        border: none
        border-radius: 28px
        background: #E9A21A
        color: #FFF
        font-family: "Roboto", sans-serif
        font-size: 20px
        font-weight: 400
        text-transform: uppercase
</style>
