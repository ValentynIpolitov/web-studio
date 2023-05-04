<template>
    <button class="btn">  
       <slot />
    </button>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.btn {
    background-color: #85D5EB;
    width: fit-content;
    cursor: pointer;
    border: 3px solid transparent;
    @apply px-5 py-3 shadow-sm transition ease-in-out duration-300 rounded leading-snug whitespace-nowrap text-base font-semibold text-white;

    &:hover {
        color: #85D5EB;
        border: 3px solid #85D5EB;
        background: transparent;
    }
}

.btn.btn-sm {
  @apply px-4 py-2 text-sm;
}

.btn.btn-lg {
  @apply text-lg px-8 py-4;
}

.btn-primary {
  @apply text-white;
  background-color: #85D5EB;
  &:hover {
    color: #85D5EB;
    border: 3px solid #85D5EB;
    background: transparent;
  }
}

.btn-secondary {
    background: transparent;
    border: 3px solid #85D5EB;
    color: #85D5EB;

    &:hover {
        color: white;
        border: 3px solid white;
    }
}
</style>
