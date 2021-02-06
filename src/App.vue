<template>
  <h2>fullname - {{firstName}} {{lastName}}</h2>
  <h2>computed fullname - {{fullName}}</h2>
  <div>
    <h2>computed total - {{total}}</h2>
    <button @click="addItem">Add</button>
  </div>

  <template v-for='item in items' :key='item.id'>
    <h2 v-if='item.price > 100'>{{item.id}}.{{item.price}}</h2>
  </template>
  <!-- original solution -->

  <h2 v-for='item in expensiveItems' :key='item.id'>
    {{item.id}}
  </h2>
  <!-- conditional render list of value -->
  <!-- computed properties with v-for -->
  <!-- cashed and from the view to recalculate the value -->

  <button @click="changeName">change</button>

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
          price: 100
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
    },
    changeName(){
      this.fullName = 'qqq www'
    }
  },
  computed:{
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`
      },
      set(value) {
        const name = value.split(' ')
        this.firstName =  name[0]
        this.lastName = name[1]
      }
      // set computed properties with setter
    },
    total(){
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
    },
    expensiveItems(){
      return this.items.filter(item => item.price > 100 )
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
