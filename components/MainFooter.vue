<template>
  <footer class="footer is-dark">
    <div class="content has-text-centered">
      <p>&copy; {{ year }}, Designed &amp; Coded by hiszuk design.</p>
    </div>
  </footer>
</template>
<script>
export default {
  name: 'MainFooter',
  data() {
    return {
      year: new Date().getFullYear(),
    }
  },
}
</script>
<style scoped>
.footer {
  z-index: -1;
  position: fixed;
  bottom: 0px;
  display: block;
  width: 100vw;
}
</style>
