<template>
    <nav class="navbar z-50">
        <div class="w-40">
            <NavLink to="/">
                <img id="logo" class="w-full nav-logo" src="/images/logo_1_white_active.svg" alt="">
            </NavLink>
        </div>

        <ul class="nav-menu z-50">
            <li class="nav-item white-text-shadow hover-underline-animation">
                <NavLink to="/#our_services" @click="closeMenu()">Our services</NavLink>
            </li>
            <li class="nav-item white-text-shadow hover-underline-animation">
                <NavLink to="/#set_up_a_call" @click="closeMenu()">Technologies</NavLink>
            </li>

            <!-- <li class="nav-item white-text-shadow hover-underline-animation">
                <NavLink to="/" @click="closeMenu()">Blog</NavLink>
            </li> -->

            <li class="nav-item">
                <Button class="btn-primary">Contact us</Button>
            </li>
        </ul>

        <div class="hamburger">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </div>
    </nav>
</template>

<script setup>
import NavLink from './NavLink.vue';
import Button from '../components/Button.vue';
import { onMounted } from 'vue'

onMounted(() => {
    const hamburger = document.querySelector(".hamburger");
    const navMenu = document.querySelector(".nav-menu");

    hamburger.addEventListener("click", mobileMenu);

    const navLink = document.querySelectorAll(".nav-link");
    navLink.forEach(n => n.addEventListener("click", closeMenu));
})


function mobileMenu() {
    const hamburger = document.querySelector(".hamburger");
    hamburger.classList.toggle("active");

    const navMenu = document.querySelector(".nav-menu");
    navMenu.classList.toggle("active");
}

function closeMenu() {
    const hamburger = document.querySelector(".hamburger");
    hamburger.classList.remove("active");

    const navMenu = document.querySelector(".nav-menu");
    navMenu.classList.remove("active");
  
    // const el = this.$refs[refName]
    // el.scrollIntoView({ behavior: 'smooth' })
}

</script>

<style lang="scss" scoped>
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.hamburger {
    display: none;
}

.bar {
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    background-color: white;
}

.nav-menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-item {
    margin-left: 5rem;
    text-transform: uppercase;
}

.nav-link {
    font-size: 1.6rem;
    font-weight: 400;
    color: #475569;
}

.nav-link:hover {
    color: #482ff7;
}

.nav-logo {
    font-size: 2.1rem;
    font-weight: 500;
    color: #482ff7;
}

// when header sticky
.is-sticky {
    .bar {
        color: #85D5EB;
        background-color: #85D5EB;
    }
}

@media only screen and (max-width: 1023px) {
    .nav-menu {
        position: fixed;
        background: #5954A4 !important;
        left: -100%;
        top: 6rem;
        flex-direction: column;
        background-color: #fff;
        width: 100%;
        border-radius: 10px;
        text-align: center;
        transition: 0.3s;
        box-shadow:
            0 10px 27px rgba(0, 0, 0, 0.05);
    }

    .is-sticky .nav-menu {
        top: 4rem;
    }

    .nav-menu.active {
        left: 0;
    }

    .nav-item {
        margin: 2.5rem 0;
    }

    .hamburger {
        display: block;
        cursor: pointer;
    }

    .hamburger.active .bar:nth-child(2) {
        opacity: 0;
    }

    .hamburger.active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
    }

    .hamburger.active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
    }
}
</style>

