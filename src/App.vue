<script setup>
import { RouterView } from 'vue-router'
import { defineAsyncComponent } from 'vue'
const navbar = defineAsyncComponent(() => import('./components/navbar.vue'))
const handleLoginEvent = (flag) => (showLogin.value = flag)
</script>

<template>
    <navbar @login="handleLoginEvent"></navbar>
    <main class="container">
        <RouterView></RouterView>
    </main>
</template>

<style scoped>
    .container{
        width: 100%;
        display: flex;
        flex-direction: column;
        max-height: 100vh;
    }
</style>