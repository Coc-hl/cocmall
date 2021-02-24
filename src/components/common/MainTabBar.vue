<template>
  <tab-bar>
    <tab-bar-item path="/home">
      <template v-slot:item-icon
        ><span class="iconfont">&#xe61f;</span></template
      >
      <template v-slot:item-text><div>首页</div></template>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <template v-slot:item-icon
        ><span class="iconfont">&#xe65d;</span></template
      >
      <template v-slot:item-text><div>分类</div></template>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <template v-slot:item-icon
        ><span class="iconfont">&#xe65d;</span></template
      >
      <template v-slot:item-text><div>购物车</div></template></tab-bar-item
    >
    <tab-bar-item path="/profile">
      <template v-slot:item-icon
        ><span class="iconfont">&#xe651;</span></template
      >
      <template v-slot:item-text><div>我的</div></template></tab-bar-item
    >
  </tab-bar>
</template>

<script>
import TabBar from "./tabbar/TabBar";
import TabBarItem from "./tabbar/TabBarItem";
export default {
  name: "MainTabBar",
  components: {
    TabBar,

    TabBarItem,
  },
};
</script>

<style scoped>

</style>