<template>
    <section class="tp-apply-process-area grey-bg pb-60">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-lg-8">
                    <div id="down" class="tp-apply-process-wrapper">
                        <h3 class="tp-apply-process-title">The Application Process</h3>

                        <div v-for="(step, index) in applicationProcess" :key="index" class="tp-apply-process-box">
                            <h4 class="tp-apply-process-subtitle">
                                <span>{{ step.step }}</span>{{ step.title }}
                            </h4>
                            <p v-html="step.description"></p>

                            <NuxtLink v-if="step.linkText && step.linkHref" :to="step.linkHref" class="tp-btn mt-30">
                                {{ step.linkText }}
                            </NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';

// Define application process steps
const applicationProcess = ref([
    {
        step: 1,
        title: "Complete Application Form",
        description: `The University of Acadia uses Apply web for the processing of graduate applications. <br> Proceed to the link below to create an Apply web account, submit an application review a <br> submitted application, and access post-submission functionality.`,
        linkText: "Application Form",
        linkHref: "/university-application-form",
    },
    {
        step: 2,
        title: "Confirmation of Application",
        description: `Admissions requirements vary by program. Please consult the <a href="#"> program website </a> to verify which information is required to complete the application.`,
    },
    {
        step: 3,
        title: "Application Review",
        description: `QRC will review your application to confirm you meet our requirements. If so, you will 
      then be asked to complete an interview as part of the review process.`,
    },
    {
        step: 4,
        title: "Application Interview",
        description: `Interviews are usually completed over the phone with a member of the Academic Team.
      The purpose of the interview is to get to know you better, hear about your future plans, understand
      why you are interested in the course.`,
    },
    {
        step: 5,
        title: "Payment of Fees",
        description: `At the end of the application, you will be required to pay the registration fee and the 
      testing fee before continuing to the next step.`,
    },
]);
</script>