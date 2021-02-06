// passing props

<template>
  <div>
    {{ name }} is {{heroName}}
  </div>
</template>

<script>
  export default {
    name: 'Great',
    props:['name', 'heroName']
  }
</script>

<style scoped>

</style>

