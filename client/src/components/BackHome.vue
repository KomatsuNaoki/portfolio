<template>
  <h3 @click="goHome()">Homeに戻る</h3>
</template>

<script>
export default {
  name: 'BackHome',
  methods: {
    goHome () {
      console.log('hello')
      this.$router.push('/')
    }
  }
}
</script>

<style>
h3 {
    position: absolute;
    right: 10px;
    bottom: 0;
}
</style>
