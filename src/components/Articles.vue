<template>
  <div v-if="isPublic">
    <h2 v-bind='$attrs'>{{title}}</h2> 
    <!-- add non prop attributes with v-bind -->
    <h2>likes - {{likes + 1}}</h2>
    <h2>is public - {{isPublic ? 'yes' : 'NO'}}</h2>
  </div>
</template>

<script>
  export default {
    name: 'Articles',
    props: {
       title: {
         type: String,
         required: true,
         default: 'default'
       }, // set required attribute and add default value
       likes: Number,
       isPublic: Boolean
    },// use objects to specify the type of props
    inheritAttrs: false // remove inheriated attrs on the root div element
  }
</script>

<style lang="scss" scoped>

</style>