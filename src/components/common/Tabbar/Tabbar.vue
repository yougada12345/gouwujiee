<template>
  <div id="tabbar">
   <slot></slot>
          <TabBarItem path="/home" active-color="rgba(191, 35, 113, 1)">
<!--            未点击时的图片-->
            <template v-slot:slot-img>
               <img src="@/assets/img/tabbar/Home.svg" alt="">
            </template>
<!--            点击时的图片-->
            <template v-slot:slot-active-img>
              <img src="@/assets/img/tabbar/Home2.svg" alt="">
            </template>
            <template v-slot:slot-text>
              <div>首页</div>
            </template>
          </TabBarItem>

          <TabBarItem path="/category" active-color="rgba(191, 35, 113, 1)">
            <template v-slot:slot-img>
              <img src="@/assets/img/tabbar/Category.svg" alt="">
            </template>
            <template v-slot:slot-active-img>
              <img src="@/assets/img/tabbar/Category2.svg" alt="">
            </template>
            <template v-slot:slot-text>
              <div>分类</div>
            </template>
          </TabBarItem>

          <TabBarItem path="/shopcart" active-color="rgba(191, 35, 113, 1)">
            <template v-slot:slot-img>
              <img src="@/assets/img/tabbar/shop-cart.svg" alt="">
            </template>
            <template v-slot:slot-active-img>
              <img src="@/assets/img/tabbar/shop-cart2.svg" alt="">
            </template>
            <template v-slot:slot-text>
              <div>购物车</div>
            </template>
          </TabBarItem>

          <TabBarItem path="/profile" active-color="rgba(191, 35, 113, 1)">
            <template v-slot:slot-img>
              <img src="@/assets/img/tabbar/Profile.svg" alt="">
            </template>
            <template v-slot:slot-active-img>
              <img src="@/assets/img/tabbar/Profile2.svg" alt="">
            </template>
            <template v-slot:slot-text>
              <div>我的</div>
            </template>
          </TabBarItem>
  </div>
</template>

<script>
  import TabBarItem from './Tab-bar-item'
  export default {
    name: "Tabbar",
    components:{
      TabBarItem
    }
  }
</script>

<style scoped>
   /*@import "../../assets/css/base.css";*/
   #tabbar{
     width: 100%;
     bottom: 0;
     display: flex;
     justify-content: space-around;
     background: #f6f6f6;
     box-shadow: 0 -1px 1px rgba(100,100,100,.1);
     position: fixed;
   }
   .tab-bar-item img{
     height: 24px;
     width: 24px;
   }
</style>
