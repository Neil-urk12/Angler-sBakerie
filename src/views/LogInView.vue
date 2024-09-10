<script setup>
import { RouterLink } from 'vue-router';
import login from "../components/signIn.vue";
import navbar from '../components/navbar.vue';
import { ref } from 'vue';
const showLogin = ref(false);
const handleLoginEvent = (flag) => showLogin.value = flag;
</script>

<template>
    <navbar @login="handleLoginEvent"></navbar>
    <section class="introductory-section">
        <div class="intro-text">
            <h5>Branded Bread Baked By the Beach</h5>
            <h1>Angler's Bakerie</h1>
            <p  class="moreYap">Imagine the taste of freshly baked bread infused with the salty breeze of the sea—crisp on the outside, soft on the inside, and bursting with coastal flavor. Each bite is like a little piece of paradise, straight from my beachside oven to your table.</p>
            <p class="lessYap">The taste of freshly baked bread infused with the salty breeze of the sea—crisp on the outside, soft on the inside, and bursting with coastal flavor.</p>
            <!-- <p>Picture this: golden crusts with a hint of sea salt, warm and buttery, fresh from my beachside oven where every loaf bakes to perfection under the sun. The unique blend of ocean air and artisanal craftsmanship creates a taste so delightful, it’ll turn every meal into a seaside escape.</p> -->
            <div class="intro-main-text">
                <RouterLink class="btn">Order Now</RouterLink>
                <RouterLink class="price">$2 |<span>Regular Price</span></RouterLink>
            </div>
        </div>
        <div class="intro-img">
            <img src="C:\neil\Code\VueDBMSTestApp\AnglersBakerie\src\assets\imgs\pixelbread.png" alt="" loading="lazy">
        </div>
        <div class="icons">
            <RouterLink><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1024 1024" id="facebook"><path fill="#1877f2" d="M1024,512C1024,229.23016,794.76978,0,512,0S0,229.23016,0,512c0,255.554,187.231,467.37012,432,505.77777V660H302V512H432V399.2C432,270.87982,508.43854,200,625.38922,200,681.40765,200,740,210,740,210V336H675.43713C611.83508,336,592,375.46667,592,415.95728V512H734L711.3,660H592v357.77777C836.769,979.37012,1024,767.554,1024,512Z"></path><path fill="#fff" d="M711.3,660,734,512H592V415.95728C592,375.46667,611.83508,336,675.43713,336H740V210s-58.59235-10-114.61078-10C508.43854,200,432,270.87982,432,399.2V512H302V660H432v357.77777a517.39619,517.39619,0,0,0,160,0V660Z"></path></svg></RouterLink>
            <RouterLink><svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 101.996 102" id="instagram"><defs><radialGradient id="a" cx="13.551" cy="102.482" r="133.147" gradientUnits="userSpaceOnUse"><stop offset=".09" stop-color="#fa8f21"></stop><stop offset=".78" stop-color="#d82d7e"></stop></radialGradient><radialGradient id="b" cx="61.859" cy="107.051" r="104.938" gradientUnits="userSpaceOnUse"><stop offset=".64" stop-color="#8c3aaa" stop-opacity="0"></stop><stop offset="1" stop-color="#8c3aaa"></stop></radialGradient></defs><path fill="url(#a)" d="M34,51A17,17,0,1,1,51,68,17,17,0,0,1,34,51m-9.191,0A26.188,26.188,0,1,0,51,24.812,26.187,26.187,0,0,0,24.812,51M72.1,23.774a6.12,6.12,0,1,0,6.122-6.118h0a6.123,6.123,0,0,0-6.12,6.118M30.4,92.513a28.187,28.187,0,0,1-9.471-1.754,15.85,15.85,0,0,1-5.866-3.815,15.735,15.735,0,0,1-3.815-5.862A28.161,28.161,0,0,1,9.49,71.611c-.247-5.376-.3-6.991-.3-20.61s.053-15.23.3-20.61a28.374,28.374,0,0,1,1.754-9.471,15.85,15.85,0,0,1,3.815-5.866,15.718,15.718,0,0,1,5.866-3.815A28.161,28.161,0,0,1,30.4,9.484c5.376-.247,6.991-.3,20.6-.3s15.23.053,20.61.3a28.373,28.373,0,0,1,9.471,1.754,15.8,15.8,0,0,1,5.866,3.815,15.8,15.8,0,0,1,3.815,5.866,28.162,28.162,0,0,1,1.754,9.471c.247,5.38.3,6.991.3,20.61s-.049,15.23-.3,20.61a28.294,28.294,0,0,1-1.754,9.471,16.886,16.886,0,0,1-9.681,9.677,28.161,28.161,0,0,1-9.471,1.754c-5.376.247-6.991.3-20.61.3s-15.23-.049-20.6-.3M29.974.309A37.4,37.4,0,0,0,17.595,2.678,25.015,25.015,0,0,0,8.56,8.56a24.918,24.918,0,0,0-5.883,9.034A37.407,37.407,0,0,0,.309,29.974C.058,35.412,0,37.15,0,51S.058,66.588.309,72.026A37.405,37.405,0,0,0,2.678,84.405,24.931,24.931,0,0,0,8.56,93.44a25.076,25.076,0,0,0,9.034,5.883,37.43,37.43,0,0,0,12.379,2.369c5.441.247,7.176.309,21.026.309s15.588-.058,21.026-.309a37.405,37.405,0,0,0,12.379-2.369A26.075,26.075,0,0,0,99.322,84.405a37.3,37.3,0,0,0,2.369-12.379c.247-5.442.3-7.176.3-21.026s-.058-15.588-.3-21.026a37.394,37.394,0,0,0-2.369-12.379A25.08,25.08,0,0,0,93.44,8.56a24.955,24.955,0,0,0-9.03-5.883A37.347,37.347,0,0,0,72.03.309C66.593.062,64.854,0,51,0s-15.59.058-21.03.309"></path><path fill="url(#b)" d="M34,51A17,17,0,1,1,51,68,17,17,0,0,1,34,51m-9.191,0A26.188,26.188,0,1,0,51,24.812,26.187,26.187,0,0,0,24.812,51M72.1,23.774a6.12,6.12,0,1,0,6.122-6.118h0a6.123,6.123,0,0,0-6.12,6.118M30.4,92.513a28.187,28.187,0,0,1-9.471-1.754,15.85,15.85,0,0,1-5.866-3.815,15.735,15.735,0,0,1-3.815-5.862A28.161,28.161,0,0,1,9.49,71.611c-.247-5.376-.3-6.991-.3-20.61s.053-15.23.3-20.61a28.374,28.374,0,0,1,1.754-9.471,15.85,15.85,0,0,1,3.815-5.866,15.718,15.718,0,0,1,5.866-3.815A28.161,28.161,0,0,1,30.4,9.484c5.376-.247,6.991-.3,20.6-.3s15.23.053,20.61.3a28.373,28.373,0,0,1,9.471,1.754,15.8,15.8,0,0,1,5.866,3.815,15.8,15.8,0,0,1,3.815,5.866,28.162,28.162,0,0,1,1.754,9.471c.247,5.38.3,6.991.3,20.61s-.049,15.23-.3,20.61a28.294,28.294,0,0,1-1.754,9.471,16.886,16.886,0,0,1-9.681,9.677,28.161,28.161,0,0,1-9.471,1.754c-5.376.247-6.991.3-20.61.3s-15.23-.049-20.6-.3M29.974.309A37.4,37.4,0,0,0,17.595,2.678,25.015,25.015,0,0,0,8.56,8.56a24.918,24.918,0,0,0-5.883,9.034A37.407,37.407,0,0,0,.309,29.974C.058,35.412,0,37.15,0,51S.058,66.588.309,72.026A37.405,37.405,0,0,0,2.678,84.405,24.931,24.931,0,0,0,8.56,93.44a25.076,25.076,0,0,0,9.034,5.883,37.43,37.43,0,0,0,12.379,2.369c5.441.247,7.176.309,21.026.309s15.588-.058,21.026-.309a37.405,37.405,0,0,0,12.379-2.369A26.075,26.075,0,0,0,99.322,84.405a37.3,37.3,0,0,0,2.369-12.379c.247-5.442.3-7.176.3-21.026s-.058-15.588-.3-21.026a37.394,37.394,0,0,0-2.369-12.379A25.08,25.08,0,0,0,93.44,8.56a24.955,24.955,0,0,0-9.03-5.883A37.347,37.347,0,0,0,72.03.309C66.593.062,64.854,0,51,0s-15.59.058-21.03.309"></path></svg></RouterLink>
            <RouterLink><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" id="email"><path fill="none" d="M0 0h24v24H0V0z"></path><path d="M22 6c0-1.1-.9-2-2-2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6zm-2 0l-8 5-8-5h16zm0 12H4V8l8 5 8-5v10z"></path></svg></RouterLink>
            <RouterLink><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 128 128"><g fill="#181616"><path fill-rule="evenodd" clip-rule="evenodd" d="M64 5.103c-33.347 0-60.388 27.035-60.388 60.388 0 26.682 17.303 49.317 41.297 57.303 3.017.56 4.125-1.31 4.125-2.905 0-1.44-.056-6.197-.082-11.243-16.8 3.653-20.345-7.125-20.345-7.125-2.747-6.98-6.705-8.836-6.705-8.836-5.48-3.748.413-3.67.413-3.67 6.063.425 9.257 6.223 9.257 6.223 5.386 9.23 14.127 6.562 17.573 5.02.542-3.903 2.107-6.568 3.834-8.076-13.413-1.525-27.514-6.704-27.514-29.843 0-6.593 2.36-11.98 6.223-16.21-.628-1.52-2.695-7.662.584-15.98 0 0 5.07-1.623 16.61 6.19C53.7 35 58.867 34.327 64 34.304c5.13.023 10.3.694 15.127 2.033 11.526-7.813 16.59-6.19 16.59-6.19 3.287 8.317 1.22 14.46.593 15.98 3.872 4.23 6.215 9.617 6.215 16.21 0 23.194-14.127 28.3-27.574 29.796 2.167 1.874 4.097 5.55 4.097 11.183 0 8.08-.07 14.583-.07 16.572 0 1.607 1.088 3.49 4.148 2.897 23.98-7.994 41.263-30.622 41.263-57.294C124.388 32.14 97.35 5.104 64 5.104z"/><path d="M26.484 91.806c-.133.3-.605.39-1.035.185-.44-.196-.685-.605-.543-.906.13-.31.603-.395 1.04-.188.44.197.69.61.537.91zm2.446 2.729c-.287.267-.85.143-1.232-.28-.396-.42-.47-.983-.177-1.254.298-.266.844-.14 1.24.28.394.426.472.984.17 1.255zM31.312 98.012c-.37.258-.976.017-1.35-.52-.37-.538-.37-1.183.01-1.44.373-.258.97-.025 1.35.507.368.545.368 1.19-.01 1.452zm3.261 3.361c-.33.365-1.036.267-1.552-.23-.527-.487-.674-1.18-.343-1.544.336-.366 1.045-.264 1.564.23.527.486.686 1.18.333 1.543zm4.5 1.951c-.147.473-.825.688-1.51.486-.683-.207-1.13-.76-.99-1.238.14-.477.823-.7 1.512-.485.683.206 1.13.756.988 1.237zm4.943.361c.017.498-.563.91-1.28.92-.723.017-1.308-.387-1.315-.877 0-.503.568-.91 1.29-.924.717-.013 1.306.387 1.306.88zm4.598-.782c.086.485-.413.984-1.126 1.117-.7.13-1.35-.172-1.44-.653-.086-.498.422-.997 1.122-1.126.714-.123 1.354.17 1.444.663zm0 0"/></g></svg></RouterLink>
        </div>
        <login v-show="showLogin"></login>
    </section>
</template>

<style scoped>
    .lessYap{
        display: none
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
        color:  rgb(54, 69, 79);
    }
    .price span {
        font-size: 1.25rem;
        font-weight: 400;
        color: rgb(0, 105, 148);
        margin-left: 10px;
    }
    .icons{
        position: absolute;
        top: 30%;
        left: 8%;
        padding: 0 7%;
        transform: translate(-50%);
    }
    .icons svg{
        display: block;
        margin: 2rem 0;
        height: 2.5rem;
        transition: 0.3s ease-in
    }
    .icons svg:hover{
        transform: scale(1.1)
    }
    /* Mobile Styles (up to 599px) */
    @media(max-width: 440px){
        .introductory-section{
            padding: 2rem 10%;
            text-align: center;
            grid-template-columns: repeat(1, 1fr);
            justify-content: center;
            gap: 0rem;
        }
        .intro-text h5{
            margin: 1rem 0 1rem 0;
            font-size: 1.25rem;
            letter-spacing: 0.5px;
        }
        .intro-text h1{
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
        .icons{
            display:none;
        }
        .price{
            font-size: 1.25rem;
            /* width: 100%; */
        }
        .price span{
            font-size: 1rem;
        }
        .moreYap{
            display: none;
        }
        .lessYap{
            display: inline;
        }
    }
    @media (max-width: 599px) {
        .introductory-section{
            text-align: center;
            grid-template-columns: repeat(1, 1fr);
            justify-content: center;
            gap: 0rem;
            padding: 80px 5% 0 5%;
        }
        .intro-text h5{
            margin: 1rem 0 1rem 0;
            font-size: 1.25rem;
            letter-spacing: 0.5px;
        }
        .intro-text h1{
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
            width: 100%
        }
        .icons{
            display:none;
        }
        .price{
            font-size: 1.25rem;
            width: 100%;
        }
        .price span{
            font-size: 1.1rem;
        }
        .moreYap{
            display: none;
        }
        .lessYap{
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