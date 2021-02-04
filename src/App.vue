<template>
  <h2>{{1 + 2 + 5}}</h2>
  <h2>{{add(1, 2, "3")}}</h2>
  <h2>{{multiply(5)}}</h2>
  <h2>{{multiplyTwo(base)}}</h2>
</template>

 
<script>
export default {
  name: 'App',
  data() {
    return{
      base: 5,
      baseValue: 10
    }
  },
  methods:{
    add(a, b, c){
      return a + b + c
    },
    multiply(num){
      return num * 5
    },
    multiplyTwo(num){
      return num * this.baseValue
      // with this value
    }
  }

  // no arrow functions
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
</style>
