<template>
  <div id="app">
    <audio id="myaudio" ref="audio" @timeupdate="musicTimeUpdate" @canplay="musicCanplay" @playing="musicOnPlaying" @ended="musicEnded" @waiting="musicOnwaiting" @pause="musicOnPause" @loadstart="loadStart"></audio>
    <v-header></v-header>
  </div>
</template>

<script>
  import header from './components/header/header.vue'
export default {
  name: 'app',
  components:{
      'v-header':header
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
body,html
  margin:0
  padding:0
  box-sizing:border-box
  background :#f0f0f0
  user-select :none
  -webkit-tap-highlight-color :transparent
  #app
    font-family :'Avenir',Helvetica,Arial,sans-serif
    -webkit-font-smoothing:antialiased
    -moz-osx-font-smoothing:frayscale
    color:#2c3e50
</style>
