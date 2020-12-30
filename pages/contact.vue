<template>
  <div>
    <page-header-middle bgimage="/images/contact.jpg" title="Contact Us" />

    <div id="main-content" class="section">
      <div class="container">
        <h1 class="title has-text-centered">contact hiszuk design</h1>
        <div class="columns">
          <div class="column"></div>
          <div class="column is-two-thirds">
            <form
              name="contact"
              method="POST"
              data-netlify="true"
              @submit.prevent="handleSubmit"
            >
              <input type="hidden" name="form-name" value="contact" />
              <b-field label="お名前">
                <b-input
                  v-model="username"
                  name="username"
                  placeholder="お名前を入力して下さい"
                  required
                  icon="account"
                ></b-input>
              </b-field>
              <b-field label="メール">
                <b-input
                  v-model="useremail"
                  name="useremail"
                  type="email"
                  placeholder="返信用メールアドレス"
                  required
                  icon="email"
                  maxlength="256"
                ></b-input>
              </b-field>
              <b-field label="件名">
                <b-input
                  v-model="title"
                  name="title"
                  required
                  maxlength="256"
                ></b-input>
              </b-field>
              <b-field message="お問い合わせ内容を入力してください">
                <b-input
                  v-model="message"
                  name="message"
                  required
                  maxlength="1000"
                  type="textarea"
                ></b-input>
              </b-field>
              <b-button
                native-type="submit"
                class="is-success"
                :loading="isSending"
                :disabled="buttonDisable"
              >
                お問い合わせ送信
              </b-button>
            </form>
          </div>
          <div class="column"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      useremail: '',
      title: '',
      message: '',
      isSubmit: false,
      isSending: false,
      isError: false,
      completeMessage: '',
    }
  },
  computed: {
    sendingClass() {
      return {
        'is-info': this.isSending,
        'is-danger': this.isError,
        'is-success': this.isSubmit,
      }
    },
    buttonDisable() {
      return !(
        this.username.length &&
        this.useremail.length &&
        this.title.length &&
        this.message.length
      )
    },
  },
  methods: {
    handleSubmit() {
      if (this.isSending) {
        return
      }
      this.isSending = true
      this.completeMessage = '送信処理中…'
      this.$buefy.toast.open({
        message: this.completeMessage,
        type: this.sendingClass,
      })
      const params = new URLSearchParams()
      params.append('form-name', 'contact')
      params.append('username', this.username)
      params.append('useremail', this.useremail)
      params.append('title', this.title)
      params.append('message', this.message)
      this.$axios
        .$post('/', params)
        .then(() => {
          this.completeMessage = 'お問い合わせを送信しました！'
          this.resetForm()
          this.isSubmit = true
          this.$buefy.toast.open({
            message: this.completeMessage,
            type: this.sendingClass,
          })
        })
        .catch((err) => {
          this.completeMessage = 'お問い合わせの送信が失敗しました'
          this.isError = true
          this.$buefy.toast.open({
            message: `${this.completeMessage} : ${err}`,
            type: this.sendingClass,
            duration: 15000,
          })
        })
        .finally(() => {
          this.isSubmit = false
          this.isSending = false
          this.isError = false
        })
    },

    resetForm() {
      this.username = ''
      this.useremail = ''
      this.title = ''
      this.message = ''
      this.isError = false
      // this.$refs.observer.reset()
    },
  },
}
</script>

<style scoped lang="scss">
@import '~/assets/style';
#main-content {
  padding-bottom: 0px;
  background-color: $white;
  color: $dark;
}
.container {
  display: block;
  margin-bottom: 1rem;
}
</style>
