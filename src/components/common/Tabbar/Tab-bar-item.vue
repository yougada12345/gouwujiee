<template>
  <div class="tab-bar-item" @click="itemClick">
   <!-- <img src="../../assets/img/2.png" alt="">
    <div>首页</div>-->
    <slot v-if="!isActived" name="slot-img"></slot>
    <slot v-else name="slot-active-img"></slot>
    <div :style="activeStyle">
      <slot name="slot-text" ></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: "tab-bar-item",
    data(){
      return{
        // isActived:false
      }
    },
    props:{
      path:String,//传回的路径，用于路由
      activeColor:{
        type:String,
        default:'black'

      }
    },
    computed:{
      isActived(){
        return this.$route.path.indexOf(this.path)!==-1
      },
      activeStyle(){
        return this.isActived?{color: this.activeColor}:{}
      }
    },
    methods:{
      itemClick(){
        console.log('kkk')
        this.$router.push(this.path)//点击跳转
      }
    }
  }
</script>

<style scoped>
  /*@import "../../assets/css/base.css";*/
  .tab-bar-item{
    height: 49px;
    text-align: center;
  }

</style>
