<template>
    <section class="slider-area tp-slider-5-wrap">

        <div class="slider tp-slider-5-active">
            <Carousel v-bind="testi_slider_opt" v-model="currentSlide">
                <Slide v-for="(item) in slider_data" class="tp-slider-5-bg" :style="{ 'background-image': 'url(' + item.bg_img + ')' }">
                    <div class="container">
                        <div class="row">
                            <div class="col-lg-7">
                                <div class="tp-slider-5-content text-start">
                                    <span>Bienvenidos a Kaian Gym</span>
                                    <h2 class="tp-slider-5-title"> <i class="me-2" v-html="item.title.text_1"></i>
                                        <span :style="{ color: '#FBF17B' }">
                                          {{ item.title.text_2 }}
                                            <img src="/images/shape/bottom-line/slider-5-line-1.svg" alt="">
                                        </span>
                                        {{ item.title.text_3 }}
                                    </h2>
                                    <div class="tp-slider-5-btn">
                                        <nuxt-link class="tp-btn-white" href="/contact">SUMATE A ENTRENAR</nuxt-link>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </Slide>
            </Carousel>
        </div>

        <div class="slider tp-slider-5-arrow">
            <Carousel v-bind="testi_nav_opt" v-model="currentSlide" ref="carouselRef">
                <Slide v-for="(nav) in nav_data" class="tp-slider-5-next">
                    <div class="tp-slider-5-thumb-sm" @click="slideTo(nav.id - 1)">
                        <img :src="nav.img" alt="">
                        <span>{{ nav.id <= 9 ? '0' + nav.id : nav.id }}</span>
                        <div class="tp-slider-5-next-hover"></div>
                    </div>
                </Slide>
            </Carousel>
        </div>

    </section>
</template>

<script setup lang="ts">
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide } from 'vue3-carousel';


const currentSlide = ref(0);
const carouselRef = ref<InstanceType<typeof Carousel> | null>(null);

const slideTo = (nextSlide: number) => (currentSlide.value = nextSlide);

const testi_slider_opt = {
    itemsToShow: 1,
    wrapAround: true,
}

const testi_nav_opt = {
    itemsToShow: 3,
    wrapAround: true,
    gap: 15,
    breakpoints: {
    // 400px and up
    0: {
      itemsToShow: 1,
    },
    // 500px and up
    500: {
      itemsToShow: 2,
    },
    // 700px and up
    700: {
      itemsToShow: 3,
    },
  },
}


const slider_data = [
   {
      id: 1,
      bg_img: '/images/slider/slider-5-bg-1.jpg',
      title: {
         text_1: 'Desbloquea todo <br/> tu potencial en',
         text_2: 'Kaian',
         text_3: 'Gym'
      }
   },
   {
      id: 2,
      bg_img: '/images/slider/slider-5-bg-2.jpg',
      title: {
         text_1: 'Tenémos todo el equipo',
         text_2: 'necesario',
         text_3: 'para vos'
      }
   },
   {
      id: 3,
      bg_img: '/images/slider/slider-5-bg-3.jpg',
      title: {
         text_1: 'Construí tu mejor',
         text_2: 'Version',
         text_3: 'en Kaian Gym'
      }
   },
   {
      id: 4,
      bg_img: '/images/slider/slider-5-bg-4.jpg',
      title: {
         text_1: 'Entrena con los mejores',
         text_2: 'profesionales',
         text_3: 'del deporte'
      }
   }
];

const nav_data = [
   {
      id: 1,
      img: '/images/slider/slider-5-sm-1.jpg',
   },
   {
      id: 2,
      img: '/images/slider/slider-5-sm-2.jpg',
   },
   {
      id: 3,
      img: '/images/slider/slider-5-sm-3.jpg',
   },
   {
      id: 4,
      img: '/images/slider/slider-5-sm-4.jpg',
   }
]

</script>
