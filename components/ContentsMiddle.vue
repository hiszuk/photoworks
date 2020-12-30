<template>
  <div class="columns">
    <div v-if="isright" class="column is-3">
      <div class="spacer">&nbsp;</div>
      <div class="right-content">
        <h3 class="subtitle">{{ title }}</h3>
        <p>
          <slot name="description"></slot>
        </p>
      </div>
    </div>
    <div class="column is-9">
      <figure class="image is-3by2">
        <img loading="lazy" :src="image" :alt="title" />
      </figure>
    </div>
    <div v-if="!isright" class="column is-3">
      <div class="spacer">&nbsp;</div>
      <div class="left-content">
        <h3 class="subtitle">{{ title }}</h3>
        <p>
          <slot name="description"></slot>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      require: false,
      default: '/images/480x320.png',
    },
    title: {
      type: String,
      require: false,
      default: '',
    },
    isright: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<style scoped lang="scss">
@import '~/assets/style';

.columns {
  padding-top: 2rem;
  padding-bottom: 1rem;
  background-color: $dark;
  color: $white;
}
.subtitle {
  color: $white;
  font-size: 1em;
  font-weight: 700;
  padding-right: 0.7em;
}
img {
  object-fit: cover;
}
p {
  font-size: 0.9em;
  font-weight: 100;
  line-height: 1.8em;
}
@media screen and (min-width: $tablet) {
  .spacer {
    margin-top: 20vw;
  }
  .left-content {
    margin-right: 3rem;
  }
  .right-content {
    text-align: right;
    margin-left: 3rem;
  }
}
@media screen and (max-width: $tablet) {
  .left-content,
  .right-content {
    margin: 0.5rem 1rem;
  }
}
</style>
