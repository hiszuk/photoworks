<template>
  <div class="page-header" :style="`background-image: url('${bgimage}')`">
    <div class="container">
      <h1 class="title">{{ title }}</h1>
      <h2 class="subtitle">{{ subtitle }}</h2>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    bgimage: {
      type: String,
      require: false,
      default: '',
    },
    title: {
      type: String,
      default: 'Title',
    },
    subtitle: {
      type: String,
      default: '',
    },
    description: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped lang="scss">
@import '~/assets/style';

.page-header {
  height: 50vh;
  margin: 0;
  background-color: $dark;
  background-size: cover;
  color: $white;
  position: relative;
}
.page-header::before {
  content: '';
  position: absolute;
  top: 0px;
  bottom: 0px;
  left: 0px;
  right: 0px;
  background: inherit;
  filter: grayscale(50%) brightness(0.7);
}
h1.title {
  color: $white;
  font-weight: 700;
}
h2.subtitle {
  color: white;
  font-weight: 500;
  font-size: 2em;
}
p {
  // position: relative;
  float: right;
  font-size: 1.1em;
  font-weight: 100;
}
@media screen and (min-width: $tablet) {
  .container {
    position: relative;
    top: calc(50vh / 2 - 3em);
    text-align: right;
  }
  h1.title {
    color: $light;
    font-size: 3em;
    font-weight: 500;
    text-shadow: 0 0 10px #333;
  }
  p {
    width: 370px;
  }
}
@media screen and (max-width: $tablet) {
  .container {
    margin-left: 1rem;
    margin-right: 1rem;
    top: calc(50vh / 2 - 3em);
    text-align: left;
  }
}
</style>
