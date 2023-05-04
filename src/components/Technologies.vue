<template>
    <section class="w-full bg-main-2">
        <div class="container m-auto px-6 py-6 flex flex-col items-center justify-start gap-y-8 md:items-start">
            <h2>Technologies</h2>
            <div class="w-full flex flex-col justify-start items-center gap-y-8 md:flex-row md:justify-center md:gap-x-32	">
                <div>
                    <IconReact class="w-36 h-auto"></IconReact>
                    <h3 class="text-center">React</h3>
                </div>

                <div>
                    <IconVue class="w-36 h-auto"></IconVue>
                    <h3 class="text-center">Vue.js</h3>
                </div>

                <div>
                    <IconLaravel class="w-36 h-auto"></IconLaravel>
                    <h3 class="text-center">Laravel</h3>
                </div>
            </div>
        </div>
    </section>
</template>
  
<script setup>
import IconReact from './icons/IconReact.vue';
import IconVue from './icons/IconVue.vue';
import IconLaravel from './icons/IconLaravel.vue';
</script>
  
<style lang="scss" scoped></style>
  