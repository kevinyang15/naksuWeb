<template>
    <section class="profile__area pt-120 pb-120">
        <div class="container">
            <div class="profile__inner p-relative">
                <div class="row">
                    <div class="col-xxl-4 col-lg-4">
                        <div class="profile__tab mr-40">
                            <!-- nav tabs for profile area -->
                            <my-account-navs />
                            <!-- nav tabs for profile area -->
                        </div>
                    </div>
                    <div class="col-xxl-8 col-lg-8">
                        <div class="profile__tab-content">
                            <div class="tab-content" id="profile-tabContent">

                                <div class="tab-pane fade show active" id="nav-profile" role="tabpanel"
                                    aria-labelledby="nav-profile-tab">
                                    <!-- Profile main dashboard -->
                                    <my-account-profile-main/>
                                    <!-- Profile main dashboard -->
                                </div>

                                <div class="tab-pane fade" id="nav-information" role="tabpanel"
                                    aria-labelledby="nav-information-tab">
                                    <div class="profile__info">
                                        <h3 class="profile__info-title">Personal Details</h3>
                                        <div class="profile__info-content">
                                            <!-- profile info update form -->
                                            <form-profile-info-update/>
                                            <!-- profile info update form -->
                                        </div>
                                    </div>
                                </div>

                                <div class="tab-pane fade" id="nav-password" role="tabpanel"
                                    aria-labelledby="nav-password-tab">
                                    <div class="profile__password">
                                        <!-- change password form -->
                                        <form-change-password/>
                                        <!-- change password form -->
                                    </div>
                                </div>

                                <div class="tab-pane fade" id="nav-address" role="tabpanel"
                                    aria-labelledby="nav-address-tab">
                                    <my-account-profile-address/>
                                </div>

                                <div class="tab-pane fade" id="nav-order" role="tabpanel"
                                    aria-labelledby="nav-order-tab">
                                    <!-- my orders area -->
                                    <my-account-orders/>
                                    <!-- my orders area -->
                                </div>

                                <div class="tab-pane fade" id="nav-notification" role="tabpanel"
                                    aria-labelledby="nav-notification-tab">
                                    <!-- notification area -->
                                    <my-account-notification/>
                                    <!-- notification area -->
                                </div>

                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">

</script>