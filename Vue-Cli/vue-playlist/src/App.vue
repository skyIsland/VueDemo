<!--1.模板：html结构-->
<template>
  <div id="app">
   <h2>{{ title }}</h2>
   <users></users>
  </div>
</template>

<!--2.行为：处理逻辑-->
<script>
// 局部注册组件
import Users from './components/Users'


export default {
  name: 'App',
  data:function(){
    return {
      title:'脚手架项目学习中...'
    }
  },
  components:{
    'users':Users
  }
}
</script>

<!-- 3.样式：解决样式 -->
<style>

</style>
