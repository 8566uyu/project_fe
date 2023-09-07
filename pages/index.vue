<template>
  <div>
    <div>Welcome!</div>
    <div v-if="accessToken">{{ accessToken }}</div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  computed: {
    // Vuex Store 정의한 state 변수와 이름을 동일하게 맞춰야 합니다.
    accessToken () {
      return this.$store.state.accessToken
    }
  }
}
</script>
