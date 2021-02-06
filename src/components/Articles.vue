<template>
  <div v-if="isPublic">
    <h2>{{title}}, likes - {{likes + 1}}, is public - {{isPublic ? 'yes' : 'NO'}}</h2>
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
    }// use objects to specify the type of props
  }
</script>

<style lang="scss" scoped>

</style>