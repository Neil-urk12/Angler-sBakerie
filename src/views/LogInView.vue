<script setup>
import { RouterLink } from 'vue-router';
import login from "../components/signIn.vue";
</script>

<template>
    <section class="introductory-section">
        <div class="intro-text">
            <h5>Branded Bread Baked By the Beach</h5>
            <h1>Angler's Bakerie</h1>
            <p>Imagine the taste of freshly baked bread infused with the salty breeze of the sea—crisp on the outside, soft on the inside, and bursting with coastal flavor. Each bite is like a little piece of paradise, straight from my beachside oven to your table.</p>
            <!-- <p>Picture this: golden crusts with a hint of sea salt, warm and buttery, fresh from my beachside oven where every loaf bakes to perfection under the sun. The unique blend of ocean air and artisanal craftsmanship creates a taste so delightful, it’ll turn every meal into a seaside escape.</p> -->
            <div class="intro-main-text">
                <RouterLink class="btn">Order Now</RouterLink>
                <RouterLink class="price">$2 |<span>Regular Price</span></RouterLink>
            </div>
        </div>
        <div class="intro-img">
                <img src="C:\neil\Code\VueDBMSTestApp\TestSystemDBMS\src\assets\imgs\pixelbread.png" alt="" loading="lazy">
        </div>
        <login></login>
    </section>
</template>

<style scoped>
    section {
        padding: 0 14%;
    }
    .introductory-section {
        position: relative;
        width: 100%;
        height: 100vh;
        background: rgb(240, 230, 140);
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        align-items: center;
        gap: 5rem;
    }
    .intro-img img {
        width: 100%;
        height: auto;
    }
    .intro-text h1 {
        text-align: center;
        font-size: 3rem;
        font-weight: 700;
        margin: 1rem 0;
        background-color: rgb(255, 97, 56);
    }
    .intro-text h5 { 
        font-size: 1.2rem;
        font-weight: 400;
        letter-spacing: 1px;
    }
    .intro-text p {
        width: 100%;
        max-width: 38.75rem;
        font-size: 1rem;
        line-height: 32px;
        margin: 0 0 40px 0;
    }
    .intro-main-text {
        display: flex;
        align-items: center;
    }
    .btn {
        display: inline-block;
        padding: 0.5rem 1.5rem;
        background: rgb(255, 97, 56);
        border: 2px solid rgb(255, 97, 56);
        border-radius: 0.5rem;
        font-size: 1.5rem;
        font-weight: 600;
        margin-right: 1.25rem;
        transition: 0.3s ease-in;
        color: white;
    }
    .btn:hover {
        transform: scale(1.1);
        background-color: rgb(0, 105, 148);
        border: rgb(0, 105, 148);
    }
    .price {
        display: flex;
        align-items: center;
        font-size: 2rem;
        font-weight: bold;
        color:  rgb(54, 69, 79);
    }
    .price span {
        font-size: 1.1rem;
        font-weight: 400;
        color: rgb(0, 105, 148);
        margin-left: 10px;
    }
</style>