<template>
 
  <h2>volume tracker (0 - 20)</h2>
  <h3>Current volume {{volume}}</h3>
  <div>
    <button @click='volume += 2'>Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>

  <input type='text' v-model='movie'/>
  <div>
    <p>movie title</p>
    <input type='text' v-model='movieInfo.title'>
  </div>
  <div>
    <p>movie actor</p>
    <input type='text' v-model='movieInfo.actor'/>
  </div>

  <button @click='movieList.push("bat4")'>push new movie</button>
</template>



 
<script>
export default {
  name: 'App',
  data() {
    return{
      volume: 0,
      movie: 'batman',
      movieInfo: {
        title: '',
        actor:''
      },
      movieList: [
        'bat',
        'bat2',
        'bat3'
      ]
    }
  },
  methods: {},
  computed:{},
  watch: {
    volume(newValue, oldValue) {
      if (oldValue < newValue && newValue === 16){
        alert('volume is too high')
      }
    },
    movie: {
      handler(newValue){
        console.log(`calling api=${newValue}`)
      },
      immediate: true
      // handler will run after the page is loaded
    },
    movieInfo: {
      handler(newValue){
        console.log(`movie title: ${newValue.title}, movie actor: ${newValue.actor}`)
      },
      deep: true
      // watch deep nested properties
    },
    movieList: {
      handler(){
        console.log(this.movieList)
      },
      deep: true
    } 
    // adding item doesn't change the reference of the array,so need deep
    // watch array with deep
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
