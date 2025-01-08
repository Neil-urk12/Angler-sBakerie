<script setup>
import { ref } from 'vue'
const emit = defineEmits(['login'])

let showLogin = ref(false)
const toggle = () => {
    showLogin.value = !showLogin.value
    emit('login', showLogin.value)
}
</script>

<template>
   <header>
        <router-link to="/">
            <div class="logo">
                <img src="\src\assets\imgs\logo.png" alt="Logo" loading="lazy">
                <h1>Bakerie</h1>
            </div>
        </router-link>
        <ul class="navbar">
            <router-link to="/about">About</router-link>
            <router-link to="/membership">Membership</router-link>
            <router-link to="/events">Events</router-link>
            <router-link to="/contact">Contact</router-link>
        </ul>

        <div class="right-btns">
            <button class="nav-btn" @click="toggle">Sign In</button>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M0 96C0 78.3 14.3 64 32 64l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 128C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 288c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32L32 448c-17.7 0-32-14.3-32-32s14.3-32 32-32l384 0c17.7 0 32 14.3 32 32z"/></svg>
        </div>
    </header>
</template>

<style scoped>
    header{
        position: fixed;
        width: 100%;
        top: 0;
        right: 0;
        z-index: 100;
        padding: 0.5rem 5%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        background: rgb(0, 105, 148);
    }
    h1{
        font-size: 3rem;
    }
    .logo{
        display: flex;
        height: auto;
        align-items: center;
    }
    .logo img{
        width: 100%;
        margin: 0 0.5rem 0 0;
        height: 4rem;
    }
    .navbar{
        display: flex; 
    }
    a{
        position: relative;
        color: black;
        font-size: 1.25rem;
        margin: 0 1rem;
        overflow: hidden;
        transition: color 0.25 ease-in;
    }
    a:hover{
        color: rgb(159, 226, 191)
    }
    a::after {
        content: '';
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0.2px;
        height: 2px; 
        transform: translateX(-100%);
        background: transparent; 
        transition: transform 0.35s ease-in;
    }
    a:hover::after {
        transform: translateX(0);
        background: rgb(255, 97, 56)
    }
    .right-btns{
        display: flex;
        flex-direction: row;
    }
    button {
        position: relative;
        padding: 0.25rem 1rem;
        font-size: 1.25rem;
        font-weight: lighter;
        width: 100%;
        border: none;
        background: none;
        cursor: pointer;
        overflow: hidden;
        outline: none;
        color: black;
        z-index: 1; 
    }
    button::after {
        content: '';
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        width: 100%;
        background: rgb(255, 97, 56); 
        transform: translateX(-100%); 
        transition: transform 0.4s ease; 
        z-index: -1; 
    }
    button:hover::after {
        transform: translateX(0); 
    }
    button:hover {
        color: white;
        z-index: 1; 
    }
    svg{
        z-index: 10001;
        cursor: pointer;
        margin-left: 1.5rem;
        display: none;
    }
    /* Mobile Styles (up to 599px) */
    @media(max-width: 440px){
        .navbar{
            display:none;
        }
        .logo h1{
            font-size: 1.75rem;
        }
        .logo img{
            height: 3rem;
        }
        button{
            font-size: 1rem;
        }
        svg{
            display: block;
        }
    }
    @media (max-width: 599px) {
        .navbar{
            display:none;
        }
        .logo h1{
            font-size: 1.75rem;
        }
        .logo img{
            height: 3rem;
        }
        button{
            font-size: 1rem;
        }
        svg{
            display: block;
        }
    }
    /* Small Tablet Styles (600px to 899px) */
    @media (min-width: 600px) and (max-width: 899px) {

    }
    /* Large Tablet Styles (900px to 1199px) */
    @media (min-width: 900px) and (max-width: 1199px) {
    }
    /* Desktop Styles (1200px and above) */
    @media (min-width: 1200px) {

    }
</style>