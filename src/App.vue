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

</style>
