<template>
    <section class="pricing-area pt-115 pb-80" style="background-color: #232323;">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-lg-6">
                    <div class="tp-section-5 text-center mb-65">
                        <h5 class="tp-section-5-subtitle mb-10" style="color: white;">Planes</h5>
                        <h3 class="tp-section-5-title" style="color: white;">Cuotas mensuales</h3>
                        <p style="color: white;">Entrena con los mejores al mejor precio</p>
                    </div>
                </div>
            </div>
            <div class="row">
                <div v-for="plan in pricingPlans" :key="plan.id" class="col-lg-4 col-md-6">
                    <div class="tp-pricing-5-item mb-40 wow fadeInUp"
                        :class="{ active: plan.title === 'Pase Libre' }" :data-wow-delay="`.${plan.id}s`">
                        <div class="tp-pricing-5-head">
                            <div class="tp-pricing-5-head-text">
                                <h4 class="tp-pricing-5-head-title" >{{ plan.title }}</h4>
                                <span>{{ plan.validity }}</span>
                            </div>
                            <h2 class="tp-pricing-5-price">
                                <span>$</span> {{ plan.price }}
                                <b>{{ plan.frequency }}</b>
                            </h2>
                        </div>
                        <div class="tp-pricing-5-list">
                            <ul>
                                <li v-for="(benefit, index) in plan.benefits" :key="`benefit-${index}`" :style="{ color: plan.title === 'Pase Libre' ? 'black' : 'white' }">
                                    <span>
                                        <svg-check-two />
                                    </span>
                                    {{ benefit }}
                                </li>
                                <li v-for="(benefit, index) in plan.inactiveBenefits" :key="`inactive-${index}`"
                                    class="inactive" style="color: #c2c2c2;">
                                    <span>
                                        <svg-un-check />
                                    </span>
                                    {{ benefit }}
                                </li>
                            </ul>
                        </div>
                        <div class="tp-pricing-5-btn">
                            <a class="tp-btn-4" href="#" style="color: #FBF7BA;">Elegir Plan</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">

const pricingPlans = [
    {
        id: 1,
        title: "3 veces por semana",
        validity: "Para los que quieren un cambio",
        price: 50000, // per month
        frequency: "/ Mes",
        benefits: [
        "Elegis tus clases",
            "Asesoramiento",
            "Locker y duchas",
        ],
        inactiveBenefits: ["Nutricion", "Competicion"],
    },
    {
        id: 2,
        title: "Pase Libre",
        validity: "Para llegar al otro nivel",
        price: 60000, // per month
        frequency: "/ Mes",
        benefits: [
            "Elegis tus clases",
            "Asesoramiento",
            "Locker y duchas",
            "Preparacion nivel competicion",
            "Nutricion",
        ],
        // inactiveBenefits: ["Free parking"],
    },
    {
        id: 3,
        title: "2 veces por semana",
        validity: "Perfecto para mantenerte activo",
        price: 40000, // per month
        frequency: "/ Mes",
        benefits: [
            "Elegis tus clases",
            "Asesoramiento",
            "Locker y duchas",
        ],
        inactiveBenefits: ["Nutricion", "Competicion"],
    },
];
</script>