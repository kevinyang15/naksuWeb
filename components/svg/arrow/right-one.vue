<template>
    <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M1 7H13" :stroke="clr" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
        <path d="M7 1L13 7L7 13" :stroke="clr" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
    </svg>
</template>


<script setup lang="ts">
withDefaults(defineProps<{ clr?: string }>(), {
    clr: "white",
})
</script>