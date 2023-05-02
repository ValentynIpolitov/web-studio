<template>
    <!-- change color active to amber -->
    <RouterLink
        class="text-white"
        active-class="underline"
    >
        <slot />
    </RouterLink>
</template>

<script setup>
    import { RouterLink } from 'vue-router'
</script>