<template>
 <div>
   <vheader></vheader>
   <div class="tab">
   <router-link to="/Foo">商品</router-link>
   <router-link to='/Bar'>评论</router-link>
   <router-link to="/sel">商家</router-link>
  </div>
  <router-view></router-view>
   <div class="content">i am content</div>
 </div>
 
</template>

<script>
import header from './components/header/head.vue'
const Foo = { template: '<div>foo</div>' }
const Bar = { template: '<div>bar</div>' }
const sel = { template: '<div>sel</div>' }
export default{
  components:{
    "vheader":header,
    Foo,
    Bar,
    sel
  }
}
</script>

<style>
.tab{
  display: flex;
  width:100%;
  height: 40px;
  line-height: 40px;
  justify-content: space-around;
}
.tab-item{
   flex: 1;
  text-align: center;
}
</style>
