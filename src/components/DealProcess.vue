<template>
    <section class="w-full bg-main-1">
        <div class="container m-auto px-6 py-6 flex flex-col items-center justify-start gap-y-8 md:items-start">
            <h2>Deal process</h2>

            <div class="w-full flex flex-col justify-start items-center gap-8 md:flex-row md:justify-between md:flex-wrap">
                <!-- step #1 -->
                <div class="set-up-a-call-card">
                    <div class="w-full px-4 py-5 gap-y-6 bg-white rounded custom-shadow flex flex-col justify-start items-center md:w-64 md:h-80">
                        <span class="text-4xl font-semibold">01</span>
                        
                        <h3 class="text-xl uppercase">Set up a call</h3>
    
                        <IconSetUpACall class="w-full h-auto" />
                    </div>
                </div>

                <!-- step #2 -->
                <div class="discuss-card">
                    <div class="w-full px-4 py-5 gap-y-6 bg-white rounded custom-shadow flex flex-col justify-start items-center md:w-64 md:h-80">
                        <span class="text-4xl font-semibold">02</span>
                        
                        <h3 class="text-xl uppercase">Discuss</h3>
    
                        <IconDiscuss class="w-full h-auto" />
                    </div>
                </div>

                <!-- step #3 -->
                <div class="create-design-card">
                    <div class="w-full px-4 py-5 gap-y-6 bg-white rounded custom-shadow flex flex-col justify-start items-center md:w-64 md:h-80">
                        <span class="text-4xl font-semibold">03</span>
                        
                        <h3 class="text-xl uppercase">Create design</h3>
    
                        <IconCreateDesign class="w-full h-auto" />
                    </div>
                </div>

                <!-- step #4 -->
                <div class="implement-design-card">
                    <div class="w-full px-4 py-5 gap-y-6 bg-white rounded custom-shadow flex flex-col justify-start items-center md:w-64 md:h-80">
                        <span class="text-4xl font-semibold">04</span>
                        
                        <h3 class="text-xl uppercase">Implement design</h3>
    
                        <IconImplementDesign class="w-full h-auto" />
                    </div>
                </div>

                <!-- step #5 -->
                <div class="online-card">
                    <div class="w-full px-4 py-5 gap-y-6 bg-white rounded custom-shadow flex flex-col justify-start items-center md:w-64 md:h-80">
                        <span class="text-4xl font-semibold">05</span>
                        
                        <h3 class="text-xl uppercase">You are ONLINE</h3>
    
                        <IconOnline class="w-full h-auto" />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import IconSetUpACall from './icons/IconSetUpACall.vue';
import IconDiscuss from './icons/IconDiscuss.vue';
import IconCreateDesign from './icons/IconCreateDesign.vue'
import IconImplementDesign from './icons/IconImplementDesign.vue'
import IconOnline from './icons/IconOnline.vue'
</script>

<style lang="scss" scoped>

.card {
    position: relative;
    z-index: 10;
    span {
        color: #85D5EB;
    }

    &::before {
        content: '';
        position: absolute;
        width: 100%;
        height: auto;
        top: 0;
        bottom: 0;
        left: 10px;
        border-radius: 10px;
        background: #85D5EB;
        filter: blur(5px);
        z-index: -1;
        
    }
}
.set-up-a-call-card {
    @extend .card;

    span {
        color: #85EBD3;
    }

    &::before {
        background: #85EBD3;
    }
}

.discuss-card {
    @extend .card;
    
    span {
        color: #85D5EB;
    }

    &::before {
        background: #85D5EB;
    }
}

.create-design-card {
    @extend .card;
    
    span {
        color: #85EB95;
    }

    &::before {
        background: #85EB95;
    }
}

.implement-design-card {
    @extend .card;
    
    span {
        color: #CAEB85;
    }

    &::before {
        background: #CAEB85;
    }
}

.online-card {
    @extend .card;
    
    span {
        color: #EBD585;
    }

    &::before {
        background: #EBD585;
    }
}

</style>
