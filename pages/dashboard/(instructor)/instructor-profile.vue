<template>
    <div>
        <nuxt-layout name="layout-nine" :dashboardLayout="true">

            <!-- banner area start -->
            <dashboard-banner />
            <!-- banner area end -->

            <dashboard-content-wrapper>

                <!-- fact area start -->
                <div class="tp-profile-wrapper">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="tp-dashboard-section">
                                <h2 class="tp-dashboard-title">My Profile</h2>
                            </div>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-12">
                            <div class="tp-profile-box">
                                <div class="tp-profile-wrap">
                                    <ul>
                                        <li v-for="(item, index) in profileData" :key="index">
                                            <div class="tp-profile-info d-flex">
                                                <div class="tp-profile-info-tag">
                                                    <span>{{ item.label }}</span>
                                                </div>
                                                <div class="tp-profile-info-details">
                                                    <span :class="item.label === 'Biography' ? 'details-zone' : ''">
                                                        {{ item.value }}
                                                    </span>
                                                </div>
                                            </div>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- fact area end -->

            </dashboard-content-wrapper>

        </nuxt-layout>
    </div>
</template>

<script setup lang="ts">
definePageMeta({
    layout: false,
});
useSeoMeta({ title: "Instructor Profile - Acadia" });


const profileData = [
    { label: 'Registration Date', value: 'October 06, 2024 8:30 am' },
    { label: 'First Name', value: 'Indigo' },
    { label: 'Last Name', value: 'Violet' },
    { label: 'Username', value: 'Instructor' },
    { label: 'Email', value: 'example@gmail.com' },
    { label: 'Phone Number', value: '+670 413 90 762' },
    { label: 'Skill/Occupation', value: 'Full Stack Developer' },
    {
        label: 'Biography',
        value: 'I have a degree in Journalism with over 15 years of work experience in the field. Throughout the years, I have worked in several well-known institutions and published several books on that are available.',
    },
];
</script>
