<template>
    <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M7.22221 13.4444C10.6586 13.4444 13.4444 10.6586 13.4444 7.22221C13.4444 3.78578 10.6586 1 7.22221 1C3.78578 1 1 3.78578 1 7.22221C1 10.6586 3.78578 13.4444 7.22221 13.4444Z" :stroke="clr" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" /> <path d="M15.0004 15L11.6171 11.6167" :stroke="clr" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
    </svg>
</template>

<script setup lang="ts">
type Props = { clr?: string }
withDefaults(defineProps<Props>(), {
    clr: "currentColor",
})
</script>