<template>
  <b-navbar type="is-dark" fixed-top centered>
    <template slot="brand">
      <b-navbar-item href="/" class="ml-6"> PHOTO WORKS </b-navbar-item>
    </template>
    <template slot="start">
      <b-navbar-item href="/">
        <b-icon icon="image-multiple" size="is-small"></b-icon>&nbsp; WORKS
      </b-navbar-item>
      <b-navbar-item href="/about">
        <b-icon icon="account-multiple" size="is-small"></b-icon>&nbsp; ABOUT US
      </b-navbar-item>
      <b-navbar-item href="/contact">
        <b-icon icon="contacts" size="is-small"></b-icon>&nbsp; CONTACT US
      </b-navbar-item>
    </template>
    <template slot="end">
      <div class="buttons mr-6">
        <!-- <b-button type="is-dark" icon-right="twitter" /> -->
        <b-button
          type="is-dark"
          icon-right="instagram"
          @click="goSite('https://www.instagram.com/katoshi_photo/')"
        />
      </div>
    </template>
  </b-navbar>
</template>

<script>
export default {
  methods: {
    goSite(url) {
      window.open(url, '_blank')
    },
  },
}
</script>

<style scoped>
.navbar-item {
  font-size: 0.9em;
  font-weight: 500;
}
.navbar-item a {
  color: white;
  opacity: 1;
}
.navbar {
  opacity: 0.7;
  /* background-color: #333; */
}
</style>
