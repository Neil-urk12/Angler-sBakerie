<script setup>

</script>

<template>
    <div class="log-in-container">
        <div>
            <h1>Sign In</h1>
        </div>
    </div>
</template>

<style scoped>
    .log-in-container{
        position: absolute;
        left: 50%;
        top: 50%;
        display: flex;
        align-items: center;
        /* justify-content: center; */
        padding: 1.5rem 1rem;
        flex-direction: column;
        transform: translate(-50%, -50%);
        background: rgba(255, 255, 255, 0.3);
        border: 1px solid rgba(255, 255, 255, 0.5);
        backdrop-filter: blur(10px);
        border-radius: 20px;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        height: 300px; 
        width: 40rem;
    }
    h1{
        font-size: 3rem;
    }
</style>