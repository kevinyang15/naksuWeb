<template>
 <svg width="11" height="12" viewBox="0 0 11 12" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M1 6H10" :stroke="clr" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
      <path d="M5.5 10.5V1.5" :stroke="clr" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
    </svg>
</template>

<script setup lang="ts">
withDefaults(defineProps<{ clr?: string }>(), {
    clr: "currentColor",
})
</script>