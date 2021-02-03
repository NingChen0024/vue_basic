<template>
  <h2 v-if="num === 0">the number if Zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>Number is {{num}}</h2>

  <template v-if="display"> 
    <h2>display is true</h2>
    <h2>display is true</h2>
    <h2>display is true</h2>
  </template>
  <!-- invisible wrapper -->
</template>
 
<script>
export default {
  name: 'App',
  data() {
    return{
        num: "eww",
        display: true
    }
  },
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
