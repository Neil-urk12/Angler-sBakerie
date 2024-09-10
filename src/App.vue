<script setup>
import { RouterView } from 'vue-router';
</script>

<template>
    <main class="container">
        <RouterView></RouterView>
    </main>
    <!-- <RouterView></RouterView> -->
</template>

<style scoped>
    .container{
        width: 100%;
        display: flex;
        flex-direction: column;
        max-height: 100vh;
    }
</style>