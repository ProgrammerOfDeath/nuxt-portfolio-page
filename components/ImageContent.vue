<template>
  <section class="image-content" :class="direction">
    <div class="columns">
      <div class="column">
        <img :src="imageSrc" alt="Image">
      </div>
      <div class="column">
        {{ textContent }}
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
    }
  },
}
</script>

<style>

</style>