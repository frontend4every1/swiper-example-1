<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
</script>

<template>
  <TheHeader />
  <router-view v-slot="{ Component }">
    <transition name="fade">
      <component :is="Component" />
    </transition>
  </router-view>
  <TheFooter />
</template>

<style lang="scss">
@import './assets/scss/main.scss';
</style>
