<template>
    <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M1 6H11" :stroke="clr" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
        <path d="M6 1L11 6L6 11" :stroke="clr" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
    </svg>
</template>


<script setup lang="ts">
withDefaults(defineProps < { clr?: string } > (), {
    clr: "#161613",
})
</script>