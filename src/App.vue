<template>
  <Great name='ning' heroName='batman'/> 
  <!-- static props -->
  <Great :name='name'/>
  <!-- dynamic props -->

  <Articles id='my-article' title='article title' :likes='30' :isPublic="true"/>
  <!-- use v-bind to pass number and bollean -->

  <ComponentA/>
  <p>{{name}}</p>
</template>

<script>
import Great from './components/Great.vue'
// import sub component
import Articles from './components/Articles.vue'
import ComponentA from './components/ComponentA.vue'

export default {
  name: 'App',
  components: {
    Great,
    Articles,
    ComponentA
  }, // informing component
  data() {
    return{
      name: 'ning'
    }
  },
  // provide: {
  //   username: 'nameTwo'
  // },
  provide() {
    return {
      userName: this.name
    }
  }, // provide values to subcomponents
    // if only pass data down to subcomponents, can use provide object
    // is data needs to be used in current page, create provide as a function returning an object
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
