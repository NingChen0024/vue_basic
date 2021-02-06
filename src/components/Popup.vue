<template>
  <div class='popup-window'>
    <p>This is a pop up</p>
    <input type='text' v-model="name"/>
    <button @click="$emit('close',name)">Close Popup</button>
    <!-- emit close event to parent component and pass data 'ning'-->
  </div>
</template>

<script>
  export default {
    name: 'Popup',
    // emits:['close'], specify close event
    emits: {
      close: (name) => {
        console.log(name)
        if (!name) {
          return false
        }else{
          return true
        }
      }
    }, // emit function validation
    data() {
      return {
        name: ''
      }
    }
  }
</script>

<style scoped>
  .popup-window{
    border: black 2px solid;
  }
</style>