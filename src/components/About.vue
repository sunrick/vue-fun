<template>
  <div id="about">
    <p class="main"> well I'm just learning how this stuff works </p>
    <p class="main"> {{ msg }} </p>
    <button @click="show = !show">
      Toggle
    </button>
    <transition
      v-on:before-enter="beforeEnter"
      v-on:enter="enter"
      v-on:leave="leave"
      v-bind:css="false">
      <p v-if="show">
        Demo
      </p>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {
      msg: "this text is coming from vue",
      show: false
    }
  },
  methods: {
    beforeEnter: function (el) {
      el.style.opacity = 0
    },
    enter: function (el, done) {
      Velocity(el, { opacity: 1, fontSize: '1.4em' }, { duration: 300 })
      Velocity(el, { fontSize: '1em' }, { complete: done })
    },
    leave: function (el, done) {
      Velocity(el, { translateX: '15px', rotateZ: '50deg' }, { duration: 600 })
      Velocity(el, { rotateZ: '100deg' }, { loop: 2 })
      Velocity(el, {
        rotateZ: '45deg',
        translateY: '30px',
        translateX: '30px',
        opacity: 0
      }, { complete: done })
    }
  }
}
</script>

<style lang="sass?indentedSyntax">
  @import '../assets/variables.sass'
  .main
    color: $primary-color
</style>
