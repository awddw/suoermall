<template>
  <div id="app">
    <router-view></router-view>
<Main-Tab-Bar></Main-Tab-Bar>
  </div>
</template>
<script>
import MainTabBar from 'components/content/mainTabbar/MianTabBar.vue'
export default {
  name: 'App',
  components: {
   MainTabBar
  }
}
</script>

<style>
@import "assets/css/base.css"
</style>
