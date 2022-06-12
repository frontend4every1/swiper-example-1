<template>
  <header class="header" id="header">
    <div class="container">
      <div class="header__inner">
        <button class="burger">
          <IconBurger class="burger__icon" />
        </button>
        <div class="logo">
          <router-link class="logo__link" :to="{ name: 'home' }">
            <img class="logo__img"
                 src="https://cdn.shopify.com/s/files/1/0689/1443/files/CLOSCA-LOGO-WEB-BLACK_130x@2x.png?v=1559116993" alt="">
          </router-link>
        </div>
        <nav class="nav">
          <ul class="nav__list">
            <li class="nav__item">
              <router-link class="nav__link" to="#">Mask</router-link>
            </li>
            <li class="nav__item">
              <router-link class="nav__link" to="#">Helmet</router-link>
            </li>
            <li class="nav__item">
              <router-link class="nav__link" to="#">Bottle</router-link>
            </li>
            <li class="nav__item">
              <router-link class="nav__link" to="#">Accessories</router-link>
            </li>
          </ul>
        </nav>
        <div class="header-icons">
          <ul class="header-icons__list">
            <li class="header-icons__item">
              <IconSearch class="header-icons__svg" />
            </li>
            <li class="header-icons__item">
              <IconUser class="header-icons__svg" />
            </li>
            <li class="header-icons__item">
              <IconBag class="header-icons__svg" />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import IconBurger from './icons/IconBurger.vue'
import IconSearch from './icons/IconSearch.vue'
import IconUser from './icons/IconUser.vue'
import IconBag from "./icons/IconBag.vue";

export default {
  name: "TheHeader",
  components: {
    IconBurger,
    IconSearch,
    IconUser,
    IconBag
  }

}
</script>

<style lang="scss" scoped>

</style>