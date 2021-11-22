<template>
  <div>
    <!-- INTRO SECTION -->
    <ImageContent 
      direction="rtl"
      image-src="/"
      :text-content="$t('introSection.textContent')"
    ></ImageContent>
  </div>
</template>

<script>

export default {
  name: 'Home',
  head() {
    return {
      title: 'Home'
    }
  }
}
</script>
