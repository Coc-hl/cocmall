<template>
  <div id="tabcontrol">
      <div v-for="(item,index) in titles" class="TCitem" :key="(item,index)" :class="{active:index===cIndex}" @click="itemClick(index)">
          <span>{{item}}</span>
      </div>
  </div>
</template>

<script>
export default {
    name:"TabControl",
    props:{
        titles:{
            type:Array,
            default(){
                return []
            }
        }
    },
    data(){
        return{
            cIndex:-1
        }
    },
    methods:{
        itemClick(index){
            this.cIndex = index
        }
    }
}
</script>

<style>
    #tabcontrol{
        display: flex;
        font-size: 14px;
        position:sticky;
        top:44px
    }
    .TCitem{
        flex:1;
        text-align: center;
        height: 40px;
        line-height: 40px;
    }
    .TCitem span{
        padding-bottom: 5px;
    }
    .active{
        color: pink;
        
    }
    .active span{
        border-bottom: pink 3px solid;
    }
</style>