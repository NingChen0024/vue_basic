<template>
  <h2>fullname - {{firstName}} {{lastName}}</h2>
  <h2>computed fullname - {{fullname}}</h2>
  <div>
    <h2>computed total - {{total}}</h2>
    <button @click="addItem">Add</button>
  </div>
</template>

 
<script>
export default {
  name: 'App',
  data() {
    return{
      firstName:'Bruce',
      lastName:'Wayue',
      items:[
        {
          id: 1,
          price: 200
        },
        {
          id: 2,
          price: 200
        },
        {
          id: 3,
          price: 600
        }
      ]
    }
  },
  methods:{
    addItem(){
      this.items.push({id: 4, price: 200})
      console.log(this.items)
    }
  },
  computed:{
    fullname(){
      return `${this.firstName} ${this.lastName}`
    },
    total(){
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
    }

    // computed properties are cashed
    // once an independent property is changed
    // the computed result will not be recalculated
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
