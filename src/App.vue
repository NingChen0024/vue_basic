<template>
  <h2>{{name}}</h2>
  <button v-on:click="changeName(), increment()">Change Name</button>

  <h2>{{count}}</h2>
  <button v-on:click="increment">Add</button>
  <button @click="count = count - 1">Minus</button>
  <div>
    <input value=/>
  </div>
</template>

 
<script>
export default {
  name: 'App',
  data() {
    return{
      name:'ning',
      count: 0,
      inputValue: 0
    }
  }, 
  methods: {
    increment(){
      this.count += 1
    },
    decrement(){
      this.count -= 1
    },
    changeName(){
      this.name = 'batman'
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
