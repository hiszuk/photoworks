<template>
  <div>
    <div id="nav">
      <navibar />
    </div>
    <div id="main">
      <nuxt />
      <div id="spacer-bottom">&nbsp;</div>
      <main-footer />
    </div>
  </div>
</template>

<script></script>

<style>
p,
h1,
h2,
h3,
h4,
h5,
h6,
p,
textarea,
input,
div {
  font-family: 'Montserrat', 'Helvetica Neue', Arial, sans-serif;
}
#main {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
}
#spacer-bottom {
  height: 7rem;
}
</style>
