<template>
  <div id="home">
    <Nav-Bar class="home-nav"><div slot="center">购物街</div></Nav-Bar>
    <Home-Swiper :banners="banners"></Home-Swiper>
    <Recommend-View :recommends="recommends"></Recommend-View>
  </div>
  
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'
import HomeSwiper from './childComps/HomeSwiper.vue'
import RecommendView from './childComps/RecommendView.vue'
import {getHomeMultidata} from 'network/home'

export default {
name:"Home",
components:{
  NavBar,
HomeSwiper,
RecommendView
},
data(){
  return{
  banners:[],
  recommends:[]
  }
},
created(){
  getHomeMultidata().then(res=>{
   this.banners=res.data.banner.list;
   this.recommends=res.data.recommend.list;
  })
}
}
</script>

<style>
.home-nav{
  background-color:var(--color-tint);
  color: #fff;
}
</style>