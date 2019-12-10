<template>
  <div class="tabBarItem" @click="itemClick">
    <div v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
  
</template>

<script>
export default {

  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle() {
      return this.isActive?{color:this.activeColor}:{}
    }
  },

  props: {
    path: String,
    activeColor: {
      type: String,
      default: '#d4237a'
    }
  },

  methods: {
    itemClick() {
      if(this.$route.path !== this.path) {
        this.$router.push(this.path)
      }

    }
  }

}
</script>

<style>
  .tabBarItem {
    flex: 1;
    text-align: center;
  }
  .tabBarItem img {
    width: 30px;
    height: 30px;
  }
</style>