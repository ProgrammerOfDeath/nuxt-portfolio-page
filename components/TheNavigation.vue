<template>
  <header class="header column">
    <b-navbar class="main-navbar bg--dark-main">
      <template #brand>
        <b-navbar-item tag="router-link" :to="{path: '/'}">
          <p>rene.hotho.dev</p>
        </b-navbar-item>
      </template>
      <template #end>
        <b-navbar-item>{{ $t('navLinks.aboutMe') }}</b-navbar-item>
        <b-navbar-item>{{ $t('navLinks.cv') }}</b-navbar-item>
        <b-navbar-item>{{ $t('navLinks.projects') }}</b-navbar-item>
      </template>
    </b-navbar>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "~/assets/scss/variables";

.header {
  padding: 10px;
}

.main-navbar {
  font-size: 1.2rem;
  .navbar-item {
    color: $font-primary;
    &:hover {
      color: $color-accent;
      background: transparent;
    }
  }
}
</style>