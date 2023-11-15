<template>
    <section class="w-full bg-main-2 overflow-hidden z-10">
        <div class="container m-auto px-6 py-6 flex flex-col items-center justify-start md:items-start">
        <!-- <div class="container m-auto px-6 py-6 flex flex-col items-center justify-start gap-y-8 md:items-start"> -->
            <h2 class="h-before h-before-2">Technologies</h2>
            <div
                class="technologies w-full flex flex-col justify-start items-center gap-y-8 md:flex-row md:justify-center md:gap-x-32	">
                <div>
                    <IconReact class="w-36 h-auto"></IconReact>
                    <h3 class="text-center animate-charcter">React</h3>
                </div>

                <div>
                    <IconVue class="w-36 h-auto"></IconVue>
                    <h3 class="text-center animate-charcter">Vue.js</h3>
                </div>

                <div>
                    <IconLaravel class="w-36 h-auto"></IconLaravel>
                    <h3 class="text-center animate-charcter">Laravel</h3>
                </div>
            </div>
        </div>
    </section>
    <div class="separation-line"></div>
</template>
  
<script setup>
import IconReact from './icons/IconReact.vue';
import IconVue from './icons/IconVue.vue';
import IconLaravel from './icons/IconLaravel.vue';
</script>
  
<style lang="scss" scoped>
.technologies {
    transition: all .3s ease;

    div {
    transition: all .3s ease;

        &:hover {
            scale: 1.1;
            &::before {
                left: 9px;
                filter: blur(3px);
            }
        }
    }
}
</style>
  