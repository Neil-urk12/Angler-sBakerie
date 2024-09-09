<script setup>
import { RouterView } from 'vue-router';
import navbar from '../src/components/navbar.vue';
</script>

<template>
    <main class="container">
        <navbar></navbar>
        <RouterView></RouterView>
    </main>
    <!-- <RouterView></RouterView> -->
</template>

<style scoped>
    .container{
        width: 100%;
        display: flex;
        flex-direction: column;
    }
</style>