<template>
  <h2 v-for="(name, index) in names" :key='index'>{{index}},{{ name }}</h2>
  <h2 v-for="(name, index) in fullNames" :key="index">{{index}} {{name.first}},{{name.second}}</h2>
  <!-- iterate over an array -->

  <template v-for="(actor, index) in actors" :key="index">
    <h2>{{actor.name}}</h2>
    <h3 v-for="(movie, index) in actor.movies" :key="index">
      {{movie}}
    </h3>
    <hr/>
  </template>
  <!-- iterate two layer array -->
  <!-- <div> also works -->

  <p v-for="(value, key, index) in myInfo" :key="value">{{value}},{{index}}, {{key}}</p>
  <!-- iterate an object -->

  <template v-for="(name, index) in names" :key="index">
    <h2 v-if="name === 'clark'">
      {{name}}
    </h2>
  </template>
  <!-- conditional list rendering -->

</template>


 
<script>
export default {
  name: 'App',
  data() {
    return{
      names:['bruce', 'clark', 'diana'],
      fullNames:[
        {first: 'brace', second: 'wayne'},
        {first: 'clark', second: 'kent'},
        {first: 'prince', second: 'diana'}
      ],
      actors:[
        {
          name: "brace",
          movies: ['batman', 'the prestige']
        },
        {
          name: "Di Caprio",
          movies: ['titanic', 'inception']
        }
      ],
      myInfo: {
        name: 'ning',
        degree: 'IT',
        age: 23
      }
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
