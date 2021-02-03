<template>
  <div>{{great}}, {{name}}</div>
  <div v-html='channel'></div>
  <div v-html='hack'></div>
  <h2 v-bind:id='headingId'>Heading</h2><!-- adding Id to element with v-bind -->
  <button v-bind:disabled='isDisabled'>disabled with v-bind:disabled</button>
  <h2 class='underline'>Underline-staticClass</h2>  <!-- static class -->
  <h2 v-bind:class='status' class='danger'>Underline-bindingClass</h2> <!-- dynamic class -->
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind:class="isNew ? 'new' : 'sold-out'">new movie</h2>
  <h2 v-bind:class="['new', 'promoted']">newly promoted</h2> <!-- classes in array -->
  <h2 v-bind:class="[isNew ? 'new' : 'sold-out', isPromoted && 'promoted']">newly promoted</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    new: isNew,
    'sold-out': !isNew
  }">object binding</h2>

  <h2 v-bind:style="{
    color: highlightColor,
    fontSize: headerSize + 'px',
    padding: '20px'
  }">Inline Style</h2>   <!-- binding inline style -->

  <h2 v-bind:style="headerStyleObj">
    object Style 
  </h2>  <!-- binding object style -->

  <div v-bind:style="[baseStyleObj, successStyleObj]">
    Success Style
  </div>  
  
   <div v-bind:style="[baseStyleObj, dangerStyleObj]">
    Danger Style
  </div>
  <!-- binding array style -->

</template>




<script>
export default {
  name: 'App',
  data() {
    return{
      great: "hello",
      name: 'ning',
      channel: '<b>rarely used</b>',
      hack:`<a href='#' onclick='alert("You have been hacked!")'>Win a Price!</a>`,
      headingId:'heading222',
      isDisabled: true,
      status:'underline',
      isPromoted: true,
      isNew: true,
      highlightColor:'orange',
      headerSize: 50,

      headerStyleObj:{
        color: 'red',
        fontSize: '50px',
        padding: '20px'
      },

      baseStyleObj: {
        fontSize: '50px',
        padding: '10px'
      },

      successStyleObj: {
        color: 'green',
        backgroundColor:'lightgreen',
        border: '1px solid green'
      },

      dangerStyleObj: {
        marginTop: '20px',
        color: 'darked',
        backgroundColor: 'red',
        border: '1px solid darked'
      }
    }
  },
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

.underline{
  text-decoration: underline;
}

.promoted{
  font-style: italic;
}

.new {
  color:olivedrab
}

.sold-out {
  color:red
}
</style>
