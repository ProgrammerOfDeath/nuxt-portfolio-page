<template>
  <section class="image-content section" :class="direction">
    <div class="columns" :class="direction">
      <div class="column">
        <img class="image-content__image" :src="imageSrc" alt="Image">
      </div>
      <div class="column is-half">
        <h2 v-if="title">{{ title }}</h2>
        <p class="font-2-0 mt-3">
          {{ textContent }}
        </p>
        <div>
          <slot name="custom-content" />
        </div>
      </div>
    </div>

  </section>
</template>

<script>
export default {
  props: {
    direction: {
      type: String,
      default: "ltr"
    },
    imageSrc: {
      type: String,
      required: true
    },
    textContent: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: false,
      default: ""
    }
  },
}
</script>

<style lang="scss">
.rtl {
  flex-direction: row-reverse;
}
.image-content {
  .image-content__image {
    padding: 0 5rem;
  }
}
</style>