<template>
  <main class="main" id="main">
    <section class="hero" id="hero">
      <div class="container">
        <SectionHero />
      </div>
    </section>
  </main>
</template>

<script>
import SectionHero from '../components/SectionHero.vue'
export default {
  name: 'HomeView',
  components: {
    SectionHero
  }
}

</script>
