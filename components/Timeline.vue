<template>
  <div class="timeline">
    <ul class="timeline__list">
      <li v-for="item, index in items" :key="index" class="timeline__item">
        <div class="time">{{ item.time }}</div>
        <h3>{{ item.title }}</h3>
        <p>{{ item.content }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      required: true
    },
  },

}
</script>

<style lang="scss">
@import "~/assets/scss/variables";

.timeline {
  border-left: 3px solid $font-primary;
  padding-left: 2rem;

  #{&}__item {
    font-size: 1.5rem;
    position: relative;
    &:not(:last-of-type) {
      margin-bottom: 3rem;
    }
    &::before {
      position: absolute;
      display: block;
      content: "";
      width: 15px;
      height: 15px;
      border-radius: 50%;
      background-color: $color-accent;
      top: calc(2rem - 8px);
      left: calc(-2rem - 8px);
    }

    .time::before {
      display: block;
      position: absolute;
      content: "";
      width: 100%;
      border-bottom: 1px solid $color-accent;
      top: 2rem;
      left: -2rem;
    }

    h3 {
      font-size: 1.5rem;
      margin-top: .8rem;
    }
    p {
      font-size: 1.2rem;
    }
  }
}
</style>