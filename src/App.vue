<template>
  <div id="app">
    <main-tab-bar></main-tab-bar>
    <router-view></router-view>
    <router-view />
  </div>
</template>
<script>
  import MainTabBar from './components/content/maintabbar/MainTabBar'
  export default {

    components: {
      MainTabBar
    }

  }
</script>

<style>
</style>
