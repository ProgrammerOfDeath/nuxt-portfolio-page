<template>
  <section class="hero-section section columns">
    <div class="hero-section__content">
      <h1>{{ $t('introSection.title') }}</h1>
      <p class="font-2-0">{{ $t('introSection.textContent') }}</p>
      <div class="hero-section__social d-flex">
        <a class="social-button--rounded" href="#">
          <b-icon
            icon="facebook"
            size="is-medium">
          </b-icon>
        </a>
        <a class="social-button--rounded" href="#">
          <b-icon
            icon="linkedin"
            size="is-medium">
          </b-icon>
        </a>
        <a class="social-button--rounded" href="#">
          <b-icon
            icon="github"
            size="is-medium">
          </b-icon>
        </a>
        <a class="social-button--rounded" href="#">
          <b-icon
            icon="email"
            size="is-medium">
          </b-icon>
        </a>
      </div>
      <div class="hero-section__cta">
        <b-button class="mr-3" type="is-primary" outlined>{{ $t('button.contact') }}</b-button>
        <b-button type="is-primary" outlined>{{ $t('button.cv') }}</b-button>
      </div>
    </div>
    <div class="hero-section__image column is-half">
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
  height: 80vh;
  h1 {
    font-size: 3rem;
    margin-bottom: 1.5rem;
  }
  .hero-section__social,
  .hero-section__cta {
    margin-top: 1.5rem;
  }
}
</style>