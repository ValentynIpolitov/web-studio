<template>
    <div
        class="w-full min-h-screen bg-[url('@/assets/main-bg.jpg')] bg-fixed bg-no-repeat bg-center bg-cover pt-36 xl:pt-16  flex flex-col	justify-center	align-start overflow-hidden z-10">
        <div class="container m-auto px-6 flex flex-col gap-y-8 xl:flex-row xl:justify-between">
            <div class="z-10 flex flex-col justify-center items-center md:items-start xl:w-1/2">
                <div class="typewriter mb-12">
                    <h1 class="text-white uppercase text-center md:text-left">Web development studio</h1>
                </div>
                <p class="text-white mb-12 text-center md:text-left">
                    “The last ten years of IT have been about changing the way people work.
                    <br>The next ten years of IT will be about transforming your business.” 
                </p>
                <NavLink to="/#our_services">
                    <Button class="btn-secondary">Our services</Button>
                </NavLink>
            </div>
            <div class="z-10 hidden xl:block xl:w-1/3">
                <img class="w-full" src="@/assets/main-img.svg" alt="">
            </div>
            <!-- Boobles for animation -->
            <div class="boobles-wrapper">
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
                <div><span class="booble"></span></div>
            </div>
        </div>
    </div>
</template>

<script setup>
import Button from './Button.vue'
import NavLink from '../shared/NavLink.vue';
</script>

<style lang="scss" scoped>
/* Typewrite effect */
.typewriter h1 {
    overflow: hidden;
    /* Ensures the content is not revealed until the animation */
    margin: 0 auto;
    /* Gives that scrolling effect as the typing happens */
    letter-spacing: .15em;
    /* Adjust as needed */
    animation:
        typing 3.5s steps(30, end),
        blink-caret .7s step-end infinite;

    font-size: 25pt;

    @media screen and (min-width: 768px) {
        font-size: 36pt;
    }

    @media screen and (min-width: 1023px) {
        white-space: nowrap;
        /* Keeps the content on a single line */
    }
}

/* The typing effect */
@keyframes typing {
    from {
        width: 0;
        /* The typwriter cursor */
        border-right: .15em solid #85D5EB;
    }

    to {
        width: 100%;
        /* The typwriter cursor */
        border-right: .15em solid #85D5EB;
    }
}

/* The typewriter cursor effect */
@keyframes blink-caret {

    from,
    to {
        border-color: transparent
    }

    50% {
        border-color: #85D5EB
    }
}

/* Boobles animation */
.boobles-wrapper {
    position: absolute;
    z-index: 5;
    min-height: 100vh;
    width: 100%;
    top: 0;
    left: 0;
}

.boobles-wrapper div {
    height: 60px;
    width: 60px;
    border: 2px solid rgba(255, 255, 255, 0.7);
    border-radius: 50px;
    position: absolute;
    top: 10%;
    left: 10%;
    animation: bobls 4s linear infinite;
}

div .booble {
    height: 10px;
    width: 10px;
    border-radius: 50px;
    background: rgba(255, 255, 255, 0.5);
    position: absolute;
    top: 20%;
    right: 20%;
}

.boobles-wrapper div:nth-child(1) {
    top: 20%;
    left: 20%;
    animation: bobls 8s linear infinite;
}

.boobles-wrapper div:nth-child(2) {
    top: 60%;
    left: 70%;
    animation: bobls 10s linear infinite;
}

.boobles-wrapper div:nth-child(3) {
    top: 40%;
    left: 40%;
    animation: bobls 3s linear infinite;
}

.boobles-wrapper div:nth-child(4) {
    top: 66%;
    left: 30%;
    animation: bobls 7s linear infinite;
}

.boobles-wrapper div:nth-child(5) {
    top: 90%;
    left: 10%;
    animation: bobls 9s linear infinite;
}

.boobles-wrapper div:nth-child(6) {
    top: 30%;
    left: 60%;
    animation: bobls 5s linear infinite;
}

.boobles-wrapper div:nth-child(7) {
    top: 70%;
    left: 20%;
    animation: bobls 8s linear infinite;
}

.boobles-wrapper div:nth-child(8) {
    top: 75%;
    left: 60%;
    animation: bobls 10s linear infinite;
}

.boobles-wrapper div:nth-child(9) {
    top: 50%;
    left: 50%;
    animation: bobls 6s linear infinite;
}

.boobles-wrapper div:nth-child(10) {
    top: 45%;
    left: 20%;
    animation: bobls 10s linear infinite;
}

.boobles-wrapper div:nth-child(11) {
    top: 10%;
    left: 70%;
    animation: bobls 9s linear infinite;
}

.boobles-wrapper div:nth-child(12) {
    top: 20%;
    left: 70%;
    animation: bobls 7s linear infinite;
}

.boobles-wrapper div:nth-child(13) {
    top: 20%;
    left: 20%;
    animation: bobls 8s linear infinite;
}

.boobles-wrapper div:nth-child(14) {
    top: 60%;
    left: 5%;
    animation: bobls 6s linear infinite;
}

.boobles-wrapper div:nth-child(15) {
    top: 90%;
    left: 70%;
    animation: bobls 9s linear infinite;
}

@keyframes bobls {
    0% {
        transform: scale(0) translateY(0) rotate(70deg);
    }

    100% {
        transform: scale(1.3) translateY(-100px) rotate(360deg);
    }
}
</style>
