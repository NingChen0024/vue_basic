<template>
  <Input type='text' v-model='name'/>
  <!-- v-model bind with customized components -->
</template>

<script>
import Input from './components/Input'
export default {
  name: 'App',
  components: {
    Input
  },
  data() {
    return{
      name: ''
    }
  }
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
