<template>
    <div>
        <nuxt-layout name="layout-eleven" :isTransparent="true">

            <!-- course banner area start -->
            <course-banner-open-filter />
            <!-- course banner area end -->

            <!-- course filter area start -->
            <course-open-filter-area />
            <!-- course filter area end -->

            <!-- banner area start -->
            <banner-one />
            <!-- banner area end -->

        </nuxt-layout>
    </div>
</template>

<script setup lang="ts">
definePageMeta({
    layout: false,
});
useSeoMeta({ title: "Course Open Filter - Acadia" });
</script>
