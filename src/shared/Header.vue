<template>
    <section class="header z-500 absolute w-full top-0 left-0">
        <header id="header" class="py-6 z-50" :class="{ 'is-sticky': isSticky }">
            <!-- header -->
            <div class="container m-auto px-6 flex justify-between">
                <img id="logo" class="w-20 xl:w-24" src="../assets/logo.png" alt="">
                <Nav />
            </div>
        </header>
    </section>
</template>

<script setup>
import Nav from './Nav.vue';
import { ref, reactive, onMounted } from 'vue'

const isSticky = ref(false);

onMounted(() => {
    window.addEventListener('scroll', updateSticky);
})

function updateSticky() {
    // Get the header
    var header = document.getElementById("header");

    // Get the offset position of the header
    var headerOffset = header.offsetTop;

    console.log('works '+window.pageYOffset+' - '+headerOffset)
    console.log(isSticky.value)
    if (window.pageYOffset > headerOffset) {
        isSticky.value = true;
        // header.classList.add("sticky")
    } else {
        isSticky.value = false;
        // header.classList.remove("sticky");
    }
}
</script>

<style lang="scss">
.is-sticky {
    position: fixed;
    top: 0;
    width: 100%;
    padding-top: 40px;

    background-color: rgba($color: #000, $alpha: 0.8);

    transition: all .2s ease, background-position 1ms;

    padding-top: 0.5rem;
    padding-bottom: 0.5rem;

    #logo {
        transform: scale(.8);
        transition: all linear .2s
    }

    @media only screen and (max-width: 1023px) {
    }
}

#logo {
    transition: all linear .2s
}

header {
    min-height: 70px;
    display: flex;
    transition: all .2s ease, background-position 1ms;

    &.is-sticky {
        padding-top: 10px;
        padding-bottom: 10px;
    }
}
</style>