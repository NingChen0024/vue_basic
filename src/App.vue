<template>
  <Great name='ning' heroName='batman'/> 
  <!-- static props -->
  <Great :name='name'/>
  <!-- dynamic props -->

  <Articles title='article title' :likes='30' :isPublic="true"/>
  <!-- use v-bind to pass number and bollean -->


</template>

<script>
import Great from './components/Great'
// import sub component
import Articles from './components/Articles.vue'

export default {
  name: 'App',
  components: {
    Great,
    Articles,
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
