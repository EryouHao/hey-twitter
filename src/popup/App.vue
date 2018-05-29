<template>
  <div class="app">
    <h1 class="header">Hey Twitter</h1>
    <b-tabs type="is-toggle" expanded @change="handleChange">
      <b-tab-item label="TimeLine" icon="google-photos">
        <time-line></time-line>
      </b-tab-item>
      <b-tab-item label="@" icon="library-music">
        <metion></metion>
      </b-tab-item>
      <b-tab-item label="Me" icon="video">
        <me></me>
      </b-tab-item>
    </b-tabs>
  </div>
</template>

<script>
import TimeLine from './TimeLine.vue'
import Metion from './Metion.vue'
import Me from './Me.vue'

export default {
  components: {
    TimeLine,
    Metion,
    Me,
  },
  data() {
    return {
      msg: 'Welcome!'
    }
  },
  methods: {
    handleChange(index) {
      console.log(index)
    },
  },
}
</script>

<style lang="stylus">
.app
  padding 16px
  width 414px
  height 736px
.header
  font-size 18px
  text-align center
  padding 16px 0
</style>
