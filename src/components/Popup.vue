<template>
  <div class='popup-window'>
    <p>This is a pop up</p>
    <button @click="$emit('close','ning')">Close Popup</button>
    <!-- emit close event to parent component and pass data 'ning'-->
  </div>
</template>

<script>
  export default {
    name: 'Popup',
    emits:['close',]
  }// specify close event
</script>

<style scoped>
  .popup-window{
    border: black 2px solid;
  }
</style>