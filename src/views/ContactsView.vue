<script setup>
import { RouterLink } from "vue-router";
import { defineAsyncComponent } from "vue";
const FacebookIcon = defineAsyncComponent(() =>
    import("../components/icons/FacebookIcon.vue")
);
const InstagramIcon = defineAsyncComponent(() =>
    import("../components/icons/InstagramIcon.vue")
);
const EmailIcon = defineAsyncComponent(() =>
    import("../components/icons/EmailIcon.vue")
);
const GithubIcon = defineAsyncComponent(() =>
    import("../components/icons/GithubIcon.vue")
);
</script>

<template>
    <section class="introductory-section">
        <div class="intro-text">
            <h5>Contact Us</h5>
            <h1>Get in Touch</h1>
            <p class="moreYap">
              We'd love to hear from you! Whether you have a question about our freshly baked bread, want to place an order, or just want to share your thoughts, feel free to reach out to us.
            </p>
            <p class="lessYap">
              Have a question or feedback? Contact us below!
            </p>
            <div class="contact-info">
              <p>Email: <a href="mailto:info@anglersbakerie.com">info@anglersbakerie.com</a></p>
              <p>Phone: <a href="tel:123-456-7890">123-456-7890</a></p>
              <p>Address: 123 Ocean Drive, Coastal City, CC 12345</p>
            </div>
          </div>
          <div class="intro-img">
            <img src="/src/assets/imgs/logo.png" alt="Angler's Bakerie Logo" loading="lazy" />
        </div>
        <div class="icons">
            <RouterLink><FacebookIcon /></RouterLink>
            <RouterLink><InstagramIcon /></RouterLink>
            <RouterLink><EmailIcon /></RouterLink>
            <RouterLink><GithubIcon /></RouterLink>
        </div>
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
  width: 80%;
  height: auto;
}
.intro-text h1 {
  text-align: center;
  font-size: 3rem;
  font-weight: 700;
  margin: 1rem 0;
  color: rgb(255, 97, 56);
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
  margin: 0 0 20px 0;
}
.contact-info {
  margin-bottom: 20px;
}
.contact-info p {
  margin: 0.5rem 0;
}
.contact-info a {
  color: rgb(0, 105, 148);
  text-decoration: none;
}
.contact-info a:hover {
  text-decoration: underline;
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
    gap: 1rem;
  }
  .intro-text h5 {
    margin: 1rem 0 1rem 0;
    font-size: 1.25rem;
    letter-spacing: 0.5px;
  }
  .intro-text h1 {
    margin: 0 0 1rem 0;
    font-size: 2rem;
  }
  .intro-text p {
    line-height: 1.5rem;
    margin: 0 0 1rem 0;
  }
  .contact-info {
    margin-bottom: 1rem;
  }
  .icons {
    display: none;
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
    gap: 1rem;
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
  }
  .intro-text p {
    line-height: 1.5rem;
    margin: 0 0 1rem 0;
  }
  .contact-info {
    margin-bottom: 1rem;
  }
  .icons {
    display: none;
  }
  .moreYap {
    display: none;
  }
  .lessYap {
    display: inline;
  }
}
</style>
```

src/router/index.js
```javascript
<<<<<<< SEARCH
  routes: [
    {
      path: "/",
      name: "Home",
      component: () => import("../views/LogInView.vue")
    },
    {
      path: "/about",
      name: "About",
      component: () => import("../views/AboutView.vue")
    }
  ]
