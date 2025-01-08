<template>
    <div class="about-us">
        <header class="header">
            <h1>About Angler's Bakerie</h1>
        </header>
        <main class="content">
            <p>
                Imagine the taste of freshly baked bread infused with the salty
                breeze of the sea—crisp on the outside, soft on the inside, and
                bursting with coastal flavor. Each bite is like a journey to the
                beach.
            </p>
            <p>
                At Angler's Bakerie, we are passionate about bringing you the
                finest baked goods, crafted with care and inspired by the ocean.
                Our bread is made using traditional methods and the freshest
                ingredients, ensuring every loaf is a masterpiece.
            </p>
        </main>
        <footer class="footer">
            <p>Visit us to experience the taste of the coast.</p>
        </footer>
    </div>
</template>

<script setup>
// You can add any reactive state or logic here if needed
</script>

<style scoped>
.about-us {
    font-family: "Arial", sans-serif;
    color: #333;
    background-color: #f4f1ea;
    padding: 20px;
    background: url("../assets/imgs/about.jpg") no-repeat center center;
    background-size: cover;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 20px;
}

.header h1 {
    font-size: 3rem;
    color: #f4f1ea; /* Light color for better contrast */
    margin-bottom: 20px;
    text-shadow: 2px 2px 4px #000000; /* Add text shadow for readability */
}

.content {
    background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent background */
    padding: 20px;
    border-radius: 10px;
}

.content p {
    font-size: 1.3rem;
    line-height: 1.7;
    color: #f4f1ea; /* Light color for better contrast */
    margin-bottom: 20px;
}

.footer {
    margin-top: 20px;
}

.footer p {
    font-size: 1.1rem;
    color: #f4f1ea; /* Light color for better contrast */
    font-style: italic;
}
</style>
