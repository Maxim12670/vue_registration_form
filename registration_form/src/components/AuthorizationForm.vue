<script setup></script>

<template>
    <div class="content">
        <form action="">
            <h2 class="content__title">Authorization</h2>
            <input type="text" name="login" class="input" placeholder="Login" required="required" />
            <input type="password" name="password" class="input" placeholder="Password" />
            <button class="button">Login</button>
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
