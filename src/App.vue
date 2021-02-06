<template>
  <Great name='ning' heroName='batman'/> 
  <!-- static props -->
  <Great :name='name'/>
  <!-- dynamic props -->

</template>

<script>
import Great from './components/Great'
// import sub component

export default {
  name: 'App',
  components: {
    Great,
  }, // informing component
  data() {
    return{
      name: 'ningpp'
    }
  },
  methods: {},
  computed:{},
  watch: {}
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
