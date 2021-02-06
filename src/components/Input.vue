<template>
  <div>
    <input 
      type='text' 
      :value='modelValue'
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>

<script>
  export default {
    name: 'Input ',
    props:{
      modelValue: String
    }
  }
</script>

<style scoped>
  input[type='text']{
    display: block;
    width: 400px;
    font-size: 14px;
    background-color: cornsilk;
    border: darkcyan 1px solid;
  }
</style>