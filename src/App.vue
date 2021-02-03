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

  <h2 v-show="showElement">Using v-show</h2> 
  <!-- keep the element and set display to nono in DOM -->
  <!-- more efficient when toggleing -->

  <h2 v-if="showElement">Using v-show</h2> 
  <!-- remove the element from dom if v-if==false -->
  <!-- its efficient if condition is unlikely to change -->
  
</template>


 
<script>
export default {
  name: 'App',
  data() {
    return{
        num: "eww",
        display: true,
        showElement: true
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
