<template>
  <section class="hero-section section">
    <div class="hero-section__content">
      <h1>{{ $t('introSection.textContent') }}</h1>
    </div>
    <div class="hero-section__image">
      <img :src="imageSrc" alt="Hero Image">
    </div>
  </section>
</template>

<script>
import heroImage from '~/assets/images/hero_image.svg'
export default {
  data() {
    return {
      imageSrc: heroImage
    }
  },
}
</script>

<style lang="scss">
.hero-section {
  margin-top: 3rem;
  display: flex;
  flex-direction: column;
  @media (min-width: 768px) {
    flex-direction: row;
  }
  h1 {
    font-size: 3rem;
    margin-bottom: 1.5rem;
  }
  .hero-section__image {
    flex: 1 0 65%;
  }
}
</style>