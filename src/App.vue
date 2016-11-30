<template>
  <div id="app">
    <about></about>
  </div>
</template>

<script>
  import About from './components/About.vue'
  export default {
    name: 'app',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    components: {
      About
    }
  }
</script>

<style lang="sass?indentedSyntax">
  #app
    font-family: 'Avenir', Helvetica, Arial, sans-serif
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    text-align: center
    color: #2c3e50
    margin-top: 60px

  h1, h2
    font-weight: normal

</style>
