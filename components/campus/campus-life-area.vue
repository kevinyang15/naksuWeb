<template>
   <section class="tp-campus-life-area p-relative grey-bg pb-210">
        <div class="container">
        <div class="row">
            <div class="col-lg-12">
                <div class="tp-campus-life-title-wrap text-center wow fadeInUp" data-wow-delay=".3s">
                    <div class="tp-campus-choose-btn">
                    <p>LIFE ON CAMPUS</p>
                    <a href="#down2"><span>
                        <svg width="20" height="80" viewBox="0 0 20 80" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M10.0001 0.00111022L10.115 80.0071" stroke="currentColor" stroke-miterlimit="10"/>
                            <path d="M20 70C14.4726 70 9.99998 74.4726 9.99998 79.9999" stroke="currentColor" stroke-miterlimit="10"/>
                            <path d="M10 80C10 74.4727 5.52736 70.0001 -1.96429e-05 70.0001" stroke="currentColor" stroke-miterlimit="10"/>
                        </svg>
                    </span></a>
                    </div>
                    <h3 class="tp-campus-life-title">Together, we grow in mind, body, spirit <br>
                    and character.</h3>
                </div>
            </div>
        </div>
        </div>
        <div class="container-fluid gx-0 fix">
        <div class="row justify-content-center gx-0">
            <div class="col-lg-12">
                <div id="down2" class="tp-campus-life-slider p-relative">

                    <swiper :slides-per-view="'auto'" :space-between="130" :loop="true" :navigation="{nextEl: '.tp-campus-next',prevEl: '.tp-campus-prev'}" :modules="[Navigation]" :breakpoints="{ 1200: { spaceBetween: 130 }, 768: { spaceBetween: 80 }, 400: { spaceBetween: 50 }}" class="swiper tp-campus-life-active">
                        
                        <swiper-slide v-for="(img, i) in campus_images" :key="i">
                            <div class="tp-campus-life-thumb text-center">
                                <img :src="img" alt="gallery-img">
                            </div>
                        </swiper-slide>

                    </swiper>

                </div>
            </div>
        </div>
        </div>
        <div class="tp-campus-life-arrow">
        <div class="tp-campus-prev pointer">
            <span>
                <svg width="34" height="18" viewBox="0 0 34 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M33 9H0.999999" stroke="currentCOlor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                    <path d="M9 1L1 9L9 17" stroke="currentCOlor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </span>
        </div>
        <div class="tp-campus-next pointer">
            <span>
                <svg width="34" height="18" viewBox="0 0 34 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M1 9H33" stroke="currentCOlor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                    <path d="M25 1L33 9L25 17" stroke="currentCOlor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </span>
         </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import { Swiper,SwiperSlide } from 'swiper/vue';
import { Navigation } from 'swiper/modules';

const slider_options = {
    slidesPerView: 'auto',
    spaceBetween: 130,
    loop: true,
    navigation: {
        nextEl: ".tp-campus-next",
        prevEl: ".tp-campus-prev",
    },
    breakpoints: {
        '1200': {
            spaceBetween: 130,
        },
        '768': {
            spaceBetween: 80,
        },
        '400': {
            spaceBetween: 50,
        },
    },
};

const campus_images = [
    '/images/campus/campus/life-thumb-1.jpg', 
    '/images/campus/campus/life-thumb-2.jpg', 
    '/images/campus/campus/life-thumb-3.jpg', 
    '/images/campus/campus/life-thumb-4.jpg', 
    '/images/campus/campus/life-thumb-2.jpg' 
];
</script>