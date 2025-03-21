<template>
    <section class="category-area pb-60" style="background-color: #232323;">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-xl-8 col-lg-10">
                    <div class="tp-section text-center mb-65">
                        <!-- <h5 class="tp-section-5-subtitle mb-10">Unique Categories</h5> -->
                        <h3 class="tp-section-5-title pt-90" style="color: white;">Explora nuestras actividades</h3>
                    </div>
                </div>
            </div>
            <div class="row wow fadeInUp" data-wow-delay=".3s">
                <div v-for="(item) in category_data" :key="item.id" class="col-xl-3 col-lg-4 col-md-6">
                    <div class="tp-category-5-item mb-60">
                        <div class="tp-category-5-hover"></div>
                        <div class="tp-category-5-thumb">
                            <img :src="item.image" alt="">
                        </div>
                        <div class="tp-category-5-content">
                            <h4 class="tp-category-5-title">
                                <nuxt-link href="#">{{ item.title }}
                                    <span>
                                        <svg-arrow-right-one clr="currentColor" />
                                    </span>
                                </nuxt-link>
                            </h4>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">

const category_data = [
    {
        id: 1,
        image: "/images/category/category-5-thumb-1.jpg",
        title: "Funcional",
    },
    {
        id: 2,
        image: "/images/category/category-5-thumb-2.jpg",
        title: "Acondicionamiento Físico",
    },
    {
        id: 3,
        image: "/images/category/category-5-thumb-3.jpg",
        title: "Fuerza",
    },
    {
        id: 4,
        image: "/images/category/category-5-thumb-4.jpg",
        title: "Boxeo",
    },
    {
        id: 5,
        image: "/images/category/category-5-thumb-5.jpg",
        title: "Muay Thai",
    },
    {
        id: 6,
        image: "/images/category/category-5-thumb-6.jpg",
        title: "Crossfit",
    },
    {
        id: 7,
        image: "/images/category/category-5-thumb-7.jpg",
        title: "Sibpalki",
    },
    {
        id: 8,
        image: "/images/category/category-5-thumb-8.jpg",
        title: "Calistenia",
    },
];
</script>