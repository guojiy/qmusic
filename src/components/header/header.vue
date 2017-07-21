<template>
  <div class="header">
    <div class="header-wrapper">
      <i class="menu icon-menu" @click="showMenu"></i>
      <div class="centerMenu" @click="hideMenu">
        <router-link to="/mymusic" tag="i">
          <i class="music icon-music" :class="selectIndex===0?'active':''"></i>
        </router-link>
        <router-link to="/findmusic" tag="i">
          <i class="find icon-wangyi"></i>
        </router-link>
        <router-link to="/community" tag="i">
          <i class="community icon-community"></i>
        </router-link>
      </div>
      <i class="search icon-search"></i>
      <router-view></router-view>
    </div>
  </div>
</template>
<script>

</script>
<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/global.styl"
  .header
    position:absolute
    top:0
    left:0
    right:0
    height :50px
    z-index:10
    background :$primarycolor
    .header-wrapper
      height:100%
      background :$primarycolor
      display: flex
      align-items :center
      justify-content:space-between
      .icon-menu,.icon-search
        color: white
        font-size :26px
        padding:10px 15px
      .centermenu
        font-size:24px
        i
          margin :0 5px
          color: #eeeeee
          &.router-link-active
            i
              color: #ccafaf
          &.active
            color: #4ae0a8
          &.music
            font-size:22px
      .counter
        position:absolute
        background:green
        width:600px
        height:150px
        color:#fff
        font-size:20px
        top:0
        left:120px
        p
          height:30px
          line-height:30px
</style>
