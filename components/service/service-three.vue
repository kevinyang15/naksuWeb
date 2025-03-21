<template>
    <section class="service-area tp-service-5-wrap mb-0" style="background-color: #232323;">
        <div class="container-fluid">
            <div class="row">
                <div v-for="(item) in service_data" :key="item.id" class="col-lg-4 col-md-6">
                    <div class="tp-service-5-item text-center">
                        <div class="tp-service-5-icon">
                            <span><img :src="item.icon" :alt="item.title"></span>
                        </div>
                        <div class="tp-service-5-content">
                            <h4 class="tp-service-5-title" style="color: white;"><a href="#">{{ item.title }}</a></h4>
                            <p style="color: white;">{{ item.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">

const service_data = [
{
        id: 1,
        icon: "/images/icon/service/service-5-icon-1.svg",
        title: "Ganá Confianza",
        description:
            "Entrenar te van a ayudar a mejorar tu ánimo y mantener una mentalidad positiva.",
    },
    {
        id: 2,
        icon: "/images/icon/service/service-5-icon-2.svg",
        title: "Mejorá tu Estado de Ánimo",
        description:
            "Esforzarte en Kaian te van a ayudar a mejorar tu ánimo y mantener una mentalidad positiva.",
    },
    {
        id: 3,
        icon: "/images/icon/service/service-5-icon-3.svg",
        title: "Aumentá tu Energía",
        description:
            "Te van a ayudar a mejorar tu ánimo y mantener una mentalidad positiva.",
    }
];
</script>
