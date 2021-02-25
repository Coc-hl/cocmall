<template>
    <div class="recommend">
        <div v-for="item in recommends" :key="item" class="r">
        <a :href="item.link">
            <img :src="item.image" alt="">
            <div>{{item.title}}</div>
        </a>
        </div>
    </div>
</template>

<script>
export default {
    name: "RecommendView",
    props:{
        recommends:{
            type:Array,
            default(){
                return []
            }
        }
    }
}
</script>

<style scoped>


    .recommend{
        display: flex;
        font-size: 12px;
        padding: 15px 0 15px;
        border-bottom:#eee solid 6px
    }
    .recommend .r{
        flex: 1;
        text-align: center;
    }
    .recommend img{
        width: 70px;
        height: 70px;
        margin-bottom: 10px;
    }
</style>