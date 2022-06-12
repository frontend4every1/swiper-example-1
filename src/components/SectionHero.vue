<script setup>
import IconArrowRight from './icons/IconArrowRight.vue'
import IconPrev from './icons/IconPrev.vue'
import IconNext from './icons/IconNext.vue'
import { Navigation } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/bundle'

const slides = [
  {
    id: 1,
    idAttr: 'beach',
    subtitle: 'Closca Bottle',
    title: 'Beach',
    price: 39.90,
    descItalic: 'In 20 years, there could be more plastic in our oceans than fish.',
    desc: 'Plastic pollution injures more than 100.000 marine animals every year.It takes around 450 years for one plastic bottle to decompose.',
    btnShow: 'Shop Now',
    heroBg: 'https://cdn.shopify.com/s/files/1/0689/1443/t/34/assets/Beach_1920.jpg?v=1029210661698833530',
    heroImg: 'https://cdn.shopify.com/s/files/1/0689/1443/t/34/assets/bottle_beach.png?v=11784267851598469514'
  },
  {
    id: 2,
    idAttr: 'savanna',
    subtitle: 'Closca Bottle',
    title: 'Savanna',
    price: 39.90,
    descItalic: 'The Earth’s area affected by desertification is approx 11 times India’s size.',
    desc: 'The Savannas act as a carbon sink, absorbing CO2 from the atmosphere and helping to maintain the balance of global temperatures.',
    btnShow: 'Shop Now',
    heroBg: 'https://images.unsplash.com/photo-1613109526778-27605f1f27d2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80',
    heroImg: 'https://cdn.shopify.com/s/files/1/0689/1443/t/34/assets/savanna_OK.png?v=4783820813181844557'
  },
  {
    id: 3,
    idAttr: 'glacier',
    subtitle: 'Closca Bottle',
    title: 'Glacier',
    price: 39.90,
    descItalic: 'Glaciers contain 75% of the World\'s freshwater.',
    desc: 'The effects of melting ice glaciers are biodiversity loss, the rising of the sea level and the deficiency of freshwater, among others.',
    btnShow: 'Shop Now',
    heroBg: 'https://www.discover-the-world.com/app/uploads/2018/05/chile-patagonia-calving-glacier-is-1150x863-c-default.jpg',
    heroImg: 'https://cdn.shopify.com/s/files/1/0689/1443/t/34/assets/Glacier_OK.png?v=7185877315400411030'
  },
  {
    id: 4,
    idAttr: 'coral',
    subtitle: 'Closca Bottle',
    title: 'Coral',
    price: 39.90,
    descItalic: 'We will have lost 60% of our coral reefs by 2030.',
    desc: 'Coral reefs are essential to humans, as they protect the shorelines and are a source of nutrients and habitat for thousands of marine species.',
    btnShow: 'Shop Now',
    heroBg: 'https://images.unsplash.com/photo-1546500840-ae38253aba9b?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3260&q=80',
    heroImg: 'https://cdn.shopify.com/s/files/1/0689/1443/t/34/assets/Coral_OK.png?v=14596995446202437119'
  }
]
</script>

<template>
    <swiper
        :navigation="{nextEl: '.nextArrow', prevEl: '.prevArrow'}"
        :modules="[Navigation]"
        class="hero__slider"
        loop
    >
      <div class="hero__navigation">
        <div class="hero__arrow hero__arrow_prev prevArrow">
          <IconPrev />
        </div>
        <div class="hero__arrow hero__arrow_next nextArrow">
          <IconNext />
        </div>
      </div>
      <swiper-slide class="hero__slide" :id="slide.idAttr" v-for="(slide, idx) in slides" :key="idx">
        <div class="hero__left">
          <div class="hero__data">
            <h1 class="hero__subtitle">{{ slide.subtitle }}</h1>
            <h1 class="hero__title">{{ slide.title }}</h1>
            <h2 class="hero__price">€ {{ slide.price }}</h2>
          </div>
          <div class="hero__content">
            <div class="hero__description hero__description_italic">{{ slide.descItalic }}</div>
            <div class="hero__description">{{ slide.desc }}</div>
            <div class="hero__show">
              {{ slide.btnShow }}
              <IconArrowRight />
            </div>
          </div>
        </div>
        <div class="hero__center">
          <div class="hero__img">
            <img class="hero__bottle-bg" :src="slide.heroBg" alt="">
            <img class="hero__bottle-img" :src="slide.heroImg" />
          </div>
        </div>
      </swiper-slide>

    </swiper>
</template>


<style>

</style>