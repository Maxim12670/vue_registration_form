<script setup>
import Navigation from './components/Navigation.vue';
</script>

<template>
    <div class="form">
        <Navigation />
    </div>
</template>

<style scope lang="sass">
    @import 'assets/fonts.css'
    .form
        position: absolute
        margin: auto
        top: 0
        right: 0
        bottom: 0
        left: 0
        width: 500px
        height: min-content
        padding: 35px 42px
        border-radius: 5%
        box-shadow: 10px -10px 5px 9px rgba(139, 90, 208, 0.2)
        background: #444

</style>
