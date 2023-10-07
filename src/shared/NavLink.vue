<template>
    <!-- change color active to amber -->
    <RouterLink
        class="text-white transition ease-in-out duration-300 hover:text-cyan-400 text-sm"
        active-class=""
    >
        <slot />
    </RouterLink>
</template>

<script setup>
    import { RouterLink } from 'vue-router'
</script>