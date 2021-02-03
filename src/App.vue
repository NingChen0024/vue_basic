<template>
  <div>{{great}}, {{name}}</div>
  <div v-text='channel'></div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return{
      great: "hello",
      name: 'ning',
      channel: 'rarely used'
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
