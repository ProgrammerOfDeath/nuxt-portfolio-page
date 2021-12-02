<template>
  <div>
    <!-- HERO -->
    <HeroSection />
    <!-- WHAT I'M DOING -->
    <ImageContent
      class="mt-5"
      :title="$t('sectionDoing.title')"
      :text-content="$t('sectionDoing.content')"
      :image-src="imgDoing"
    >
      <template #custom-content>
        <div class="mt-4">
          <b-tooltip
            label="Vue.js"
            type="is-light"
          >
            <b-icon icon="vuejs" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="Node.js"
            type="is-light"
          >
            <b-icon icon="nodejs" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="Bootstrap"
            type="is-light"
          >
            <b-icon icon="bootstrap" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="JavaScript"
            type="is-light"
          >
            <b-icon icon="language-javascript" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="CSS"
            type="is-light"
          >
            <b-icon icon="language-css3" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="HTML"
            type="is-light"
          >
            <b-icon icon="language-html5" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="Symfony"
            type="is-light"
          >
            <b-icon icon="symfony" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="Python"
            type="is-light"
          >
            <b-icon icon="language-python" size="is-large"></b-icon>
          </b-tooltip>
          <b-tooltip
            label="Docker"
            type="is-light"
          >
            <b-icon icon="docker" size="is-large"></b-icon>
          </b-tooltip>
        </div>
      </template>
    </ImageContent>
  </div>
</template>

<script>
import imgSrcDoing from '~/assets/images/what_im_doing.svg'

export default {
  name: 'Home',
  data() {
    return {
      imgDoing: imgSrcDoing
    }
  },
  head() {
    return {
      title: 'Home'
    }
  },
}
</script>
