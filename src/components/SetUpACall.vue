<template>
    <section class="w-full bg-[url('@/assets/main-bg.jpg')] bg-fixed bg-no-repeat bg-center bg-cover">
        <div class="container m-auto px-6 py-6 flex flex-col items-center justify-start gap-y-4 xl:flex-row xl:justify-center xl:gap-x-12">
            <p class="text-white text-3xl text-center ">Want to learn more? Set up a free call!</p>
            <Button class="btn-secondary">Set up a call</Button>
        </div>
    </section>
</template>

<script setup>
import Button from './Button.vue'
</script>

<style lang="scss" scoped></style>
