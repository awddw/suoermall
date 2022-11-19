<template>
  <div class="recommend">
    <div v-for="(val,key) in recommends" :key="key" class="recommend-item">
      <a :href="val.link">
    <img :src="val.image" alt="">
 <div>{{val.title}}</div>
  </a>
    </div>
  </div>
</template>

<script>
export default {
name:"RecommendView",
props:{
    recommends:{
        type:Array,
    default(){
        return[]
    }
    }
    
}
}
</script>

<style>
.recommend{
    display: flex;
    text-align: center;
    width: 100%;
    font-size: 12px;
    padding: 10px 0 20px;
    border-bottom: 8px solid #eee;
}
.recommend-item{
    flex: 1;
}
.recommend-item img{
    width: 70px;
    height: 70px;
}
</style>