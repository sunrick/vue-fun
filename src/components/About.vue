<template>
  <div id="about">
    <p class="main"> well I'm just learning how this stuff works </p>
    <p class="main"> {{ msg }} </p>
  </div>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {
      msg: "this text is coming from vue"
    }
  }
}
</script>

<style lang="sass?indentedSyntax">
  @import '../assets/variables.sass'
  .main
    color: $primary-color
</style>
