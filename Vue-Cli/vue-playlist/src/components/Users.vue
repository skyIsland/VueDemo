<template>
  <div class="users">
   <ul>
       <li v-for="user in users">
           <p>
               {{ user }}
           </p>
       </li>
   </ul>
  </div>
</template>

<script>
export default {
  name: 'Users',
  data () {
    return {
      users: ['张三','李四','王五','赵六']
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
