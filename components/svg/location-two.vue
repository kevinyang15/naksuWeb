<template>
    <svg width="14" height="16" viewBox="0 0 14 16" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
            d="M12.375 6.72727C12.375 11.1818 6.6875 15 6.6875 15C6.6875 15 1 11.1818 1 6.72727C1 5.20831 1.59922 3.75155 2.66583 2.67748C3.73244 1.60341 5.17908 1 6.6875 1C8.19592 1 9.64256 1.60341 10.7092 2.67748C11.7758 3.75155 12.375 5.20831 12.375 6.72727Z"
            :stroke="clr" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
        <path
            d="M6.6888 8.63654C7.73584 8.63654 8.58464 7.78181 8.58464 6.72745C8.58464 5.67309 7.73584 4.81836 6.6888 4.81836C5.64176 4.81836 4.79297 5.67309 4.79297 6.72745C4.79297 7.78181 5.64176 8.63654 6.6888 8.63654Z"
            :stroke="clr" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
    </svg>
</template>

<script setup lang="ts">
withDefaults(defineProps<{ clr?: string }>(), {
    clr: "#84807B",
})
</script>
