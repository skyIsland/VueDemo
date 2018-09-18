<!--1.模板：html结构-->
<template>
  <div id="app">
   <app-header></app-header>
   <users></users>
   <app-footer></app-footer>
  </div>
</template>

<!--2.行为：处理逻辑-->
<script>
// 局部注册组件
import Users from './components/Users'
import Header from './components/Header'
import Footer from './components/Footer'


export default {
  name: 'App',
  data:function(){
    return {
      title:'脚手架项目学习中...'
    }
  },
  components:{
    'users':Users,
    'app-header':Header,
    'app-footer':Footer
  }
}
</script>

<!-- 3.样式：解决样式 -->
<style>
  h2{
    color:purple;
  }
</style>
