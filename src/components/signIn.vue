<script setup>
import { ref } from 'vue';
    const signUp = ref(false);
    const boxToggle = () =>{
        signUp.value = !signUp.value;
    }
</script>

<template>
    <div class="log-in-container">
        <div class="sign-in-box" v-if="!signUp">
            <h1>Sign In</h1>      
            <form class="log-in-form">
                <input type="text" placeholder="Email"><br>
                <input type="text" placeholder="********">
                <div class="submit-route-box">
                    <button class="submit" type="submit">Sign In</button>
                    <h3 @click="boxToggle">Don't have an account?<br>Register now!</h3>
                </div>
                <p>Forgot your password?</p>
            </form>
        </div>
        <div class="register" v-if="signUp">
            <h1>Register</h1>      
            <form class="log-in-form">
                <input type="email" placeholder="Email"><br>
                <input type="text" placeholder="Name"><br>
                <input type="text" placeholder="Contact Number"><br>
                <input type="password" placeholder="********"><br>
                <input type="search" placeholder="********">
                <div class="submit-route-box">
                    <button class="submit" type="submit">Sign In</button>
                    <h3 @click="boxToggle">Sign up</h3>
                </div>
                <p>Forgot your password?</p>
            </form>
        </div>
    </div>
</template>

<style scoped>
    .log-in-container{
        position: absolute;
        left: 50%;
        top: 50%;
        padding: 1.75rem 0.5rem 2.5rem 0.5rem;
        transform: translate(-50%, -50%);
        background: rgba(240, 230, 140, 0.3);
        border: 1px solid rgba(255, 255, 255, 0.5);
        backdrop-filter: blur(10px);
        border-radius: 20px;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        width: 40rem;
        text-align: left;
    }
    .sign-in-box, .register{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .log-in-form{
        width: 80%;
        margin: 0.5rem 0 0 0;
        border-radius: 22px;
        background-color: white;
        padding: 2rem;
    }
    input{
        text-align: center;
        font-size: 1.3rem;
        margin: 0 0 1rem 0;
        width: 100%;
        padding: 0.5rem 1rem;
        background: transparent;
        outline: none;
        border: 3px solid black;
        border-radius: 22px;
    }
    .submit-route-box{
        position: relative;
        margin: 0 0 0.5rem 0;
    }
    button{
        text-align: left;
        cursor: pointer;
        background: rgb(255, 97, 56);
        font-size: 1.75rem;
        color: white;
        padding: 0.25rem 1rem;
        border:  none;
        transition: 0.2s ease-in;
    }
    button:hover{
        color: black;
    }
    h3{
        position: absolute;
        right: 0;
        top: 0;
        text-align: right;
        font-size: 1.1rem;
        font-weight: 400;
        color: black;
        padding: 0.25rem;
        cursor: pointer;
    }
    h3:hover{
        color:rgb(255, 97, 56);
    }
    h1{
        font-size: 3rem;
    }
</style>