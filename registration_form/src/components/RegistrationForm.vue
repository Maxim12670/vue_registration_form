<script setup></script>

<template>
    <div class="content">
        <form action="">
            <h2 class="content__title">Create Account</h2>
            <input type="text" name="firstName" class="content__input" placeholder="First Name" required="required" />
            <input type="text" name="lastName" class="content__input" placeholder="Last Name" required="required" />
            <input type="text" name="login" class="content__input" placeholder="Login" required="required" />
            <input type="email" name="email" class="content__input" placeholder="Email" required="required" />
            <input type="password" name="password" class="content__input" placeholder="Password" />
            <input type="file" name="file" class="content__input_file" />
            <button class="content__btn">create</button>
        </form>
    </div>
</template>

<style scoped lang="sass">
    @import '../assets/fonts.css'
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
        &__btn
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
