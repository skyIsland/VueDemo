<template>
  <footer>
      <p>
          {{ title }}
      </p>
  </footer>
</template>

<script>
export default {
  name: 'app-footer',
  data () {
    return {
      title: '我只是一个来自南方的footer~'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer{
    background-color: #222;
    padding:6px;
}
p{
    color:lightgreen;
    text-align: center;    
}
</style>
