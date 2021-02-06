<template>
  <Input type='text' v-model='name'/>
  <!-- v-model bind with customized components -->

  <Card>Card content</Card>
  <Card><h2>Card head content</h2></Card>
  <Card><img src='https://i.picsum.photos/id/310/200/200.jpg?hmac=gpEKQ-zUG9L-jZga6K0jQ2NHHqqoPzMKUR-_ZmiL734'></Card>
</template>

<script>
import Input from './components/Input'
import Card from './components/Card'

export default {
  name: 'App',
  components: {
    Input,
    Card
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
