<template>
  <div class="card">
    <div class="card-image">
      <figure class="image is-4by3">
        <img :src="image" :alt="name" />
      </figure>
    </div>
    <div class="card-content">
      <div class="media">
        <div class="media-left">
          <figure class="image is-64x64">
            <img class="is-rounded" :src="avatar" :alt="name" />
          </figure>
        </div>
        <div class="media-content">
          <p class="title is-4">{{ name }}</p>
          <p class="subtitle is-6">{{ incharge }}</p>
        </div>
      </div>

      <div class="content">
        <slot name="body">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec
          iaculis mauris.
          <br />
          <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
        </slot>
      </div>
      <div class="sns">
        <slot name="footer"> </slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: false,
      default: 'John Smith',
    },
    image: {
      type: String,
      required: false,
      default: '/images/480x320.png',
    },
    avatar: {
      type: String,
      required: false,
      default: 'https://bulma.io/images/placeholders/96x96.png',
    },
    incharge: {
      type: String,
      required: false,
      default: '',
    },
  },
}
</script>

<style scoped lang="scss">
@import '~/assets/style';
.content {
  min-height: 5rem;
  font-size: 0.9em;
  line-height: 1.2em;
}
.sns {
  text-align: center;
}
</style>
