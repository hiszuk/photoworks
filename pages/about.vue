<template>
  <div>
    <page-header-middle bgimage="/images/about.jpg" title="About Us" />

    <div id="main-content" class="section">
      <div class="container has-text-centered">
        <h1 class="title">hiszuk design staff</h1>
      </div>
    </div>

    <div id="profile-cards" class="section">
      <div class="columns is-desktop is-centered">
        <div class="column">
          <profile-card
            name="Satoshi Kato"
            image="/images/profiles/satoshi_kato_img.jpg"
            avatar="/images/profiles/satoshi_kato_avatar.jpg"
            incharge="Photographer"
          >
            <template slot="body">
              <ul>
                <li>Photograph</li>
                <li>Apprentice</li>
              </ul>
            </template>
            <template slot="footer">
              <sns-icon
                type="is-success"
                icon="instagram"
                desc="インスタグラム"
                @click="click('https://www.instagram.com/katoshi_photo/')"
              ></sns-icon>
            </template>
          </profile-card>
        </div>
        <div class="column">
          <profile-card
            name="Hisakazu Kato"
            image="/images/profiles/hisakazu_kato_img.jpg"
            avatar="/images/profiles/hisakazu_kato_avatar.jpg"
            incharge="Design/Code"
          >
            <template slot="body">
              <ul>
                <li>サイトデザイン(bluma, buefy, bootstrap)</li>
                <li>コーディング(Nuxt.js, firebase, springboot)</li>
                <li>インフラエンジニア(docker, aws, netlify)</li>
              </ul>
            </template>
            <template slot="footer">
              <sns-icon
                type="is-success"
                icon="github"
                desc="Open Github repository of hiszuk"
                @click="click('https://github.com/hiszuk/')"
              ></sns-icon>
              <sns-icon
                type="is-success"
                icon="instagram"
                desc="インスタグラム"
                @click="click('https://www.instagram.com/hiszuk/')"
              ></sns-icon>
            </template>
          </profile-card>
        </div>
        <!-- <div class="column">
          <profile-card />
        </div> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    click(url) {
      window.open(url, '_blank')
    },
  },
}
</script>

<style scoped lang="scss">
@import '~/assets/style';
#main-content {
  // margin-top: 4px;
  padding-bottom: 20px;
  background-color: $white;
  color: $dark;
}
#profile-cards {
  background-color: $white;
}
.container {
  display: block;
  margin-bottom: 1rem;
}
.column {
  max-width: 500px;
}
@media screen and (min-width: $tablet) {
  #profile-cards {
    padding: 2rem 5rem 4rem;
  }
  .column {
    margin: 0 1rem;
  }
}
</style>
