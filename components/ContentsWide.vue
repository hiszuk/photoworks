<template>
  <div class="card">
    <div class="card-image">
      <figure class="image">
        <img loading="lazy" :src="image" :alt="title" />
      </figure>
    </div>
    <div class="card-content">
      <div class="content">
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
  },
}
</script>

<style scoped lang="scss">
@import '~/assets/style';

.card {
  padding-top: 7rem;
  padding-bottom: 3rem;
  background-color: $white;
  color: $black;
  text-align: center;
}
h3.subtitle {
  color: $dark;
  font-size: 1em;
  font-weight: 700;
}
p {
  font-size: 0.9em;
  font-weight: 200;
  line-height: 1.8em;
}
img {
  max-width: 100%;
  height: auto;
}
</style>
