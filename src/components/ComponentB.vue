<template>
  <div>
    ComponentB - {{userName}}
  </div>
</template>

<script>
  export default {
    name: 'ComponentB',
    inject: ['userName'] //inject values from root component
  }
</script>

<style lang="scss" scoped>

</style>