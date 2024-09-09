<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
   <header>
        <div class="logo">
            <img src="C:\neil\Code\VueDBMSTestApp\TestSystemDBMS\src\assets\imgs\logo.png" alt="Logo" loading="lazy">
            <h1>Bakerie</h1>
        </div>
        <ul class="navbar">
            <RouterLink>About</RouterLink>
            <RouterLink>Membership</RouterLink>
            <RouterLink>Events</RouterLink>
            <RouterLink>Contact</RouterLink>
        </ul>

        <div class="right-btns">
            <button class="nav-btn">Sign In</button>
            <div>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M0 96C0 78.3 14.3 64 32 64l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 128C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 288c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32L32 448c-17.7 0-32-14.3-32-32s14.3-32 32-32l384 0c17.7 0 32 14.3 32 32z"/></svg>
            </div>
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
        /* background: rgb(240, 230, 140); */
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
        color: black;
        font-size: 1.15rem;
        margin: 0 1rem;
    }
    a:hover{
        color: rgb(159, 226, 191)
    }
    .right-btns{
        display: flex;
        flex-direction: row;
    }
    button{
        margin: 0 1rem 0 0;
        font-size: 1.15rem;
        width: 5rem;
        border: none;
        background: none;
        transition: 0.3s ease-in;
        cursor: pointer;
    }
    button:hover{
        border: 2px solid rgb(15, 91, 255);
        background: rgb(15, 91, 255);
        color: white;
    }
    svg{
        z-index: 10001;
        cursor: pointer;
        margin-left: 1.5rem;
        display: none;
    }
</style>