<template>
  <div>
    <!-- HERO -->
    <HeroSection />
    <!-- WHAT I'M DOING -->
    <ImageContent
      id="skills"
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

    <!-- EDUCATION -->
    <ImageContent
      id="education"
      class="mt-5"
      title="Education"
      :image-src="imgEducation"
      direction="rtl"
    >
      <template #custom-content>
        <Timeline 
          :items="timelineItems"
        />
      </template>
    </ImageContent>
  </div>
</template>

<script>
import imgSrcDoing from '~/assets/images/what_im_doing.svg'
import imgSrcEducation from '~/assets/images/education.svg'

export default {
  name: 'Home',
  data() {
    return {
      imgDoing: imgSrcDoing,
      imgEducation: imgSrcEducation,
      timelineItems: [
        {
          time: this.$t('sectionEducation.itSpecialist.time'),
          title: this.$t('sectionEducation.itSpecialist.title'),
          content: this.$t('sectionEducation.itSpecialist.content')
        },
        {
          time: this.$t('sectionEducation.technicalAssistent.time'),
          title: this.$t('sectionEducation.technicalAssistent.title'),
          content: this.$t('sectionEducation.technicalAssistent.content')
        },
        {
          time: this.$t('sectionEducation.university.time'),
          title: this.$t('sectionEducation.university.title'),
          content: this.$t('sectionEducation.university.content')
        },
      ]
    }
  },
  head() {
    return {
      title: 'Home'
    }
  },
}
</script>
