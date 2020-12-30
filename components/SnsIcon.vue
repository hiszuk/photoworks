<template>
  <div class="sns-icon">
    <b-tooltip :label="desc" type="is-dark" position="is-top">
      <b-button :type="type" @click="click">
        <b-icon type="is-white" :icon="icon" size="is-midium"> </b-icon>
      </b-button>
    </b-tooltip>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: false,
      default: 'is-link',
    },
    desc: {
      type: String,
      required: false,
      default: 'Open as new window',
    },
  },
  methods: {
    click() {
      this.$emit('click')
    },
  },
}
</script>

<style scoped>
.sns-icon {
  display: inline;
  margin: 0 0.3em;
}
</style>
