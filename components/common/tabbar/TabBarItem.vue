<template>
  <div class="tab-bar-item" @click="itemClick">
      <!-- icon -->
      <div v-if="!isActive"><slot name="item-icon"> </slot></div>
      <!-- 活跃的icon -->
      <div v-else><slot name="item-icon-active"> </slot></div>
      <!-- 文字 -->
      <div :style="activeStyle"><slot name="item-text"> </slot></div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
      path: String,
      activeColor: {
          type: String,
          default: "#fc5979",
      },
  },
  mounted(){
      console.log(this.isActive,this.activeColor)
  },
  computed: {
      isActive() {
          //判断传过来的，是否为当前路径
          return this.$route.path.indexOf(this.path) !== -1;
      },
      activeStyle() {
          return this.isActive ? { color: this.activeColor } : {};
      },
  },
  methods: {
      itemClick() {
          this.$router.replace(this.path);
      },
  },
};
</script>

<style lang="less" scoped>
.tab-bar-item {
    img {
        width: 24px;
        height: 24px;
    }
    div:nth-child(2){
        text-align: center;
        font-size: 14px;
    }
}
</style>
