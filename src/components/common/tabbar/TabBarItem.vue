<template>
  <div class="tab-bar-item" @click="itemClick" >
    <slot name="item-icon"></slot>
    <slot name="item-text"></slot>
  </div>
  <!-- <div class="tab-bar-item">
    <span class="iconfont">&#xe61f;</span>
    <div>分类</div>
  </div> -->
  <!-- <div class="tab-bar-item">
    <span class="iconfont">&#xe7f9;</span>
    <div>分类</div>
  </div>
  <div class="tab-bar-item">
    <span class="iconfont">&#xe65d;</span>
    <div>购物车</div>
  </div>
  <div class="tab-bar-item">
    <span class="iconfont">&#xe651;</span>
    <div>我的</div>
  </div> -->
</template>

<script>
export default {
  name: "TabBarItem",
  data(){
    return{
      active:false
    }
  },
  props: {
    path:String
  },
  methods:{
    itemClick(){
      this.$router.replace(this.path).catch(err=>err)
      this.active = true
    }
  }
};
</script>

<style scoped>
@font-face {
  font-family: "iconfont";
  src: url("../../../assets/css/iconfont/iconfont.eot");
  src: url("../../../assets/css/iconfont/iconfont.eot?#iefix")
      format("embedded-opentype"),
    url("../../../assets/css/iconfont/iconfont.woff2") format("woff2"),
    url("../../../assets/css/iconfont/iconfont.woff") format("woff"),
    url("../../../assets/css/iconfont/iconfont.ttf") format("truetype"),
    url("../../../assets/css/iconfont/iconfont.svg#iconfont") format("svg");
}
.iconfont {
  font-family: "iconfont" !important;
  font-size: 16px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

}

.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
}

.active{
  background-color: pink;
}
</style>