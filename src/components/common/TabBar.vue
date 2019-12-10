<template>
  <div class="tabbar">
    <slot></slot>
  </div>
</template>

<script>
  export default {

  }
</script>

<style>
  .tabbar {
    display: flex;
    justify-content: center;
    flex-flow: row nowrap;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
  }
</style>