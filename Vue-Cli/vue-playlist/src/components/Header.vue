<template>
  <header>
      <h1>
          {{ title }}
      </h1>
  </header>
</template>

<script>
export default {
  name: 'app-header',
  data () {
    return {
      title: '我只是一个来自北方的header~'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
    background: lightgreen;
    padding:10px;
}
h1{
    color:#222;
    text-align: center;    
}
</style>
