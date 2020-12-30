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
      default: 'subtitle',
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
  height: 102vh;
  margin: 0;
  background-size: cover;
  color: $white;
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
    top: calc(100vh / 2 - 4rem);
    text-align: right;
  }
  p {
    width: 370px;
  }
}
@media screen and (max-width: $tablet) {
  .container {
    margin-left: 1rem;
    margin-right: 1rem;
    top: calc(100vh / 2 - 4rem);
    text-align: left;
  }
}
</style>
