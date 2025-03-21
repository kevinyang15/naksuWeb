<template>
    <div>
        <nuxt-layout name="layout-four">

<!-- hero area start -->
<hero-banner-four />
<!-- hero area end -->

<!-- service area start -->
<service-three />
<!-- service area end -->

<!-- category area start -->
<category-two />
<!-- category area end -->

<!-- brand area start -->
<brand-area-two />
<!-- brand area end -->

<!-- course area start -->

<!-- <course-gym-area /> -->
<!-- course area end -->

<!-- video area start -->
<video-one />
<!-- video area end -->

<!-- text slider area start -->
<text-slider />
<!-- text slider area end -->

<!-- pricing area start -->
<pricing-area />
<!-- pricing area end -->

<!-- team area start -->
<team-area-two />
<!-- team area end -->

<!-- banner area start -->
<banner-two />
<!-- banner area end -->
<contact-area />

<div class="tp-map-area">
    <div class="tp-contact-map-content">
        <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3284.4090852434456!2d-58.468280123779394!3d-34.59381567295789!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95bcb607acf3a481%3A0xd86d0f8d5a7a2c1d!2sPje.%20Fernando%20de%20Montalvo%20149%2C%20C1427%20Cdad.%20Aut%C3%B3noma%20de%20Buenos%20Aires!5e0!3m2!1ses-419!2sar!4v1742515888275!5m2!1ses-419!2sar"
            width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"
            referrerpolicy="no-referrer-when-downgrade">
        </iframe>
    </div>
</div>

</nuxt-layout>
    </div>
</template>

<script setup lang="ts">
definePageMeta({
    layout: false,
});
useSeoMeta({ title: "Kaian GYM - BOXING + FITNESS" });
</script>
