<script setup>
import { RouterLink } from "vue-router";
import { defineAsyncComponent } from "vue";
const navbar = defineAsyncComponent(() => import("../components/navbar.vue"));
const login = defineAsyncComponent(() => import("../components/signIn.vue"));
import { ref } from "vue";
const FacebookIcon = defineAsyncComponent(() => import("../components/icons/FacebookIcon.vue"));
const InstagramIcon = defineAsyncComponent(() => import("../components/icons/InstagramIcon.vue"));
const EmailIcon = defineAsyncComponent(() => import("../components/icons/EmailIcon.vue"));
const GithubIcon = defineAsyncComponent(() => import("../components/icons/GithubIcon.vue"));
const showLogin = ref(false);
const handleLoginEvent = (flag) => (showLogin.value = flag);
</script>

<template>
    <navbar @login="handleLoginEvent"></navbar>
    <section class="introductory-section">
        <div class="intro-text">
            <h5>Branded Bread Baked By the Beach</h5>
            <h1>Angler's Bakerie</h1>
            <p class="moreYap">
                Imagine the taste of freshly baked bread infused with the salty
                breeze of the sea—crisp on the outside, soft on the inside, and
                bursting with coastal flavor. Each bite is like a little piece
                of paradise, straight from my beachside oven to your table.
            </p>
            <p class="lessYap">
                The taste of freshly baked bread infused with the salty breeze
                of the sea—crisp on the outside, soft on the inside, and
                bursting with coastal flavor.
            </p>
            <!-- <p>Picture this: golden crusts with a hint of sea salt, warm and buttery, fresh from my beachside oven where every loaf bakes to perfection under the sun. The unique blend of ocean air and artisanal craftsmanship creates a taste so delightful, it’ll turn every meal into a seaside escape.</p> -->
            <div class="intro-main-text">
                <RouterLink class="btn">Order Now</RouterLink>
                <RouterLink class="price"
                    >$2 |<span>Regular Price</span></RouterLink
                >
            </div>
        </div>
        <div class="intro-img">
            <img src="/src/assets/imgs/pixelbread.png" alt="" loading="lazy" />
        </div>
        <div class="icons">
            <RouterLink
                ><FacebookIcon /></RouterLink>
            <RouterLink
                ><InstagramIcon /></RouterLink>
            <RouterLink
                ><EmailIcon /></RouterLink>
            <RouterLink
                ><GithubIcon /></RouterLink>
        </div>
        <login v-show="showLogin"></login>
    </section>
</template>

<style scoped>
.lessYap {
    display: none;
}
.introductory-section {
    padding: 0 12%;
    position: relative;
    width: 100%;
    height: 100vh;
    background: rgb(240, 230, 140);
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
    gap: 2rem;
}
.intro-img img {
    width: 100%;
    height: auto;
}
.intro-text h1 {
    text-align: center;
    font-size: 4rem;
    font-weight: 700;
    margin: 1rem 0;
    background-color: rgb(255, 97, 56);
}
.intro-text h5 {
    text-align: center;
    font-size: 1.5rem;
    font-weight: 400;
    letter-spacing: 1px;
}
.intro-text p {
    text-align: justify;
    width: 100%;
    max-width: 38.75rem;
    font-size: 1.25rem;
    line-height: 32px;
    margin: 0 0 40px 0;
}
.intro-main-text {
    display: flex;
    align-items: center;
    justify-content: center;
}
.btn {
    display: inline-block;
    padding: 0.5rem 1.5rem;
    background: rgb(255, 97, 56);
    border: 2px solid rgb(255, 97, 56);
    border-radius: 0.5rem;
    font-size: 1.5rem;
    font-weight: 600;
    margin-right: 1rem;
    transition: all 0.2s ease-in;
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
    color: rgb(54, 69, 79);
}
.price span {
    font-size: 1.25rem;
    font-weight: 400;
    color: rgb(0, 105, 148);
    margin-left: 10px;
}
.icons {
    position: absolute;
    top: 30%;
    left: 8%;
    padding: 0 7%;
    transform: translate(-50%);
}
.icons svg {
    display: block;
    margin: 2rem 0;
    height: 2.5rem;
    transition: 0.3s ease-in;
}
.icons svg:hover {
    transform: scale(1.1);
}
/* Mobile Styles (up to 599px) */
@media (max-width: 440px) {
    .introductory-section {
        padding: 2rem 10%;
        text-align: center;
        grid-template-columns: repeat(1, 1fr);
        justify-content: center;
        gap: 0rem;
    }
    .intro-text h5 {
        margin: 1rem 0 1rem 0;
        font-size: 1.25rem;
        letter-spacing: 0.5px;
    }
    .intro-text h1 {
        margin: 0 0 1rem 0;
        font-size: 2rem;
        margin: 0.5rem 0 0.5rem 0;
    }
    .intro-text p {
        line-height: 1.5rem;
        margin: 0 0 1.5rem 0;
    }
    .btn {
        padding: 0.25rem 1rem;
        font-size: 1rem;
        margin-right: 1rem;
    }
    .icons {
        display: none;
    }
    .price {
        font-size: 1.25rem;
        /* width: 100%; */
    }
    .price span {
        font-size: 1rem;
    }
    .moreYap {
        display: none;
    }
    .lessYap {
        display: inline;
    }
}
@media (max-width: 599px) {
    .introductory-section {
        text-align: center;
        grid-template-columns: repeat(1, 1fr);
        justify-content: center;
        gap: 0rem;
        padding: 80px 5% 0 5%;
    }
    .intro-text h5 {
        margin: 1rem 0 1rem 0;
        font-size: 1.25rem;
        letter-spacing: 0.5px;
    }
    .intro-text h1 {
        margin: 0 0 1rem 0;
        font-size: 2rem;
        margin: 0.5rem 0 0.5rem 0;
    }
    .intro-text p {
        line-height: 1.5rem;
        margin: 0 0 1.5rem 0;
    }
    .btn {
        padding: 0.25rem 1rem;
        font-size: 1.2rem;
        margin: 1rem 1.25rem;
        width: 100%;
    }
    .icons {
        display: none;
    }
    .price {
        font-size: 1.25rem;
        width: 100%;
    }
    .price span {
        font-size: 1.1rem;
    }
    .moreYap {
        display: none;
    }
    .lessYap {
        display: inline;
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
