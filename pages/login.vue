<template>
  <a @click="loginWithKakao">
    <img src="/kakao_login.png"/>
  </a>
</template>

<script>
export default {
  name: 'IndexPage',
  methods: {
    kakaoInit () {
      Kakao.init('83a60ac982f14c358884e30d9988efa8')// KaKao client key
      Kakao.isInitialized()
    },
    async loginWithKakao () {
      await Kakao.Auth.authorize({
        redirectUri: `${window.location.origin}/kakao-callback`
      })
    }
  },
  mounted () {
    this.kakaoInit()
  }
}
</script>
