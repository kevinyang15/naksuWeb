<template>
    <footer style="background-color: ;">
      <div :class="`tp-footer-main ${style_2 ? '' : 'grey-bg'} pt-80 pb-55`">
        <div class="container">
          <div class="row">
            <!-- Logo and Contact Section -->
            <div class="col-xl-4 col-lg-3 col-sm-6">
              <div :class="`tp-footer-widget ${style_2 ? 'tp-footer-5-col-1' : 'tp-footer-col-1'} mb-30`">
                <div class="tp-footer-widget-logo mb-20 tp-header-logo">
                  <nuxt-link to="/">
                    <img :src="style_2 ? '/images/logo/logokaian.png' : '/images/logo/logo-red.png'" alt="logo" />
                  </nuxt-link>
                </div>
                <!-- <div class="tp-footer-widget-content">
                  <p>
                    Lorem ipsum dolor sit amet, consectetur <br /> adipisc ing elit.
                  </p>
                </div> -->
                <div class="tp-footer-contact">
                  <span>Tenes consultas? Contactanos</span>
                  <a href="tel:012345678">112 158 8635</a>
                </div>
                <div class="tp-footer-contact-mail">
                  <a href="mailto:kaianboxgym@gmail.com">
                    <span>
                      <svg-email-one />
                    </span>
                    kaianboxgym@gmail.com
                  </a>
                </div>
              </div>
            </div>
  
            <!-- About Links Section -->
            <div class="col-xl-2 col-lg-3 col-sm-6">
              <div :class="`tp-footer-widget ${style_2 ? 'tp-footer-5-col-2' : 'tp-footer-col-2'} mb-30`">
                <h4 class="tp-footer-widget-title mb-20">About</h4>
                <div class="tp-footer-widget-link">
                  <ul>
                    <li v-for="link in footerLinks.link_one" :key="link.id">
                      <nuxt-link :to="link.link">{{ link.title }}</nuxt-link>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
  
            <!-- Quick Links Section -->
            <div class="col-xl-2 col-lg-2 col-sm-4">
              <div :class="`tp-footer-widget ${style_2 ? 'tp-footer-5-col-3' : 'tp-footer-col-3'} mb-30`">
                <h4 class="tp-footer-widget-title mb-20">Links rápidos</h4>
                <div class="tp-footer-widget-link">
                  <ul>
                    <li v-for="link in footerLinks.link_two" :key="link.id">
                      <nuxt-link :to="link.link">{{ link.title }}</nuxt-link>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
  
            <!-- Newsletter Section -->
            <div class="col-xl-4 col-lg-4 col-sm-8">
              <div :class="`tp-footer-widget ${style_2 ? 'tp-footer-5-col-4' : 'tp-footer-col-4'} mb-30`">
                <h4 class="tp-footer-widget-title mb-20">Nuestro Newsletter</h4>
                <div class="tp-footer-newsletter-wrap">
                  <p>Recibí info <br /> sobre eventos y competiciones</p>
                  <form @submit.prevent>
                    <div class="tp-footer-newsletter-wrapper mb-30">
                      <div :class="`tp-footer-newsletter-input ${style_2 ? 'tp-footer-5-newsletter-input' : ''}`">
                        <input type="email" placeholder="Tu email" />
                      </div>
                      <div :class="`${style_2 ? 'tp-footer-5-newsletter-submit' : 'tp-footer-newsletter-submit'}`">
                        <button :class="`${style_2 ? 'tp-btn-4' : 'tp-btn'}`" style="color: #FBF7BA">Subscribité</button>
                      </div>
                    </div>
                  </form>
                  <!-- Footer Social -->
                   <div class="tp-footer-newsletter-social">
                       <social-links/>
                   </div>
                  <!-- Footer Social -->
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
  
      <!-- Footer Bottom Section -->
      <div :class="`${style_2 ? 'tp-footer-5-bottom' : 'tp-footer-bottom'}`">
        <div class="container">
          <div class="row">
            <div class="col-lg-12">
              <div class="tp-footer-copyright text-center">
                <span>
                  © {{ new Date().getFullYear() }} <a href="#">Kaian GYM</a>. Derechos Reservados.
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script setup lang="ts">
  import { footerLinks } from "@/data/footer-links";
  
  const props = defineProps<{style_2?: boolean;}>();
  
  const style_2 = props.style_2 ?? false;
  </script>
  