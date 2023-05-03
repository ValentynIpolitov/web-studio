<template>
    <div class="w-full min-h-screen bg-[url('@/assets/main-bg.jpg')] bg-fixed bg-no-repeat bg-center bg-cover pt-16  flex flex-col	justify-center	align-start">
        <div class="container m-auto px-6">
            <div class="flex flex-col justify-center items-center md:items-start">
                <h1 class="text-white uppercase mb-12 text-center md:text-left">Web development studio</h1>
                <p class="text-white mb-12 text-center md:text-left">
                    “The last ten years of IT have been about changing the way people work. 
                    <br>The next ten years of IT will be about transforming your business.” 
                </p>
                <Button class="btn-secondary">Our services</Button>
            </div>
        </div>
    </div>
</template>

<script setup>
import Button from './Button.vue'
</script>

<style lang="scss" scoped></style>
