<template>
    <div id="home">
        <nav-bar class="home-nav"><template v-slot:center>cocMall</template></nav-bar>
        <myswiper class="myswiper">
            <template v-slot:picture1>
                <a :href="banner[0].link">
                    <img :src="banner[0].image" alt="">
                </a></template>
                            <template v-slot:picture2>
                <a :href="banner[1].link">
                    <img :src="banner[1].image" alt="">
                </a></template>
                            <template v-slot:picture3>
                <a :href="banner[2].link">
                    <img :src="banner[2].image" alt="">
                </a></template>
                            <template v-slot:picture4>
                <a :href="banner[3].link">
                    <img :src="banner[3].image" alt="">
                </a></template>

        </myswiper>
        
    </div>
</template>



<script>
import NavBar from '../../components/common/navbar/NavBar.vue'
import {getHomeMultidata} from '../../network/home'
import myswiper from '../../components/common/swiper/Swiper'
export default {
    name:"Home",
    components:{
        NavBar,
        myswiper
    },
    data(){
        return{
            banner:[],
            recommends:[],
            keywords:[],
            dkeywords:[]
        }
    },
    created(){
        getHomeMultidata().then(res=>{
            console.log(res)
            this.banner = res.data.banner.list;
            this.recommends = res.data.recommend;
        })
    }
}
</script>

<style scoped>
    .home-nav{
        background-color: skyblue;
    }
    .myswiper{
        width: 100%;
    }
    .myswiper img{
        width: 100%;
    }
</style>