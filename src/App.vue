<template>
  <p>{{formValues.name.length}}</p> 
  <!-- prevent modifier -->
  <form @submit.prevent="submitForm">
    <div>
      <label for='name'>Name</label>
      <input type='text' v-model.trim.lazy='formValues.name'/>
      <!-- <input @keyup.enter='submitForm' type='text'/> -->
      <!-- submit after press enter -->
    </div>

    <!-- text field -->
    <div>
      <label for='profile'>Profile</label>
      <input type='text' v-model='formValues.profileSummary'/>
    </div>

    <div>
      <label for='age'>Age</label>
      <input type='text' v-model.number='formValues.age'/>
    </div>

    <!-- single selection -->
    <div>
      <label for='country'>Country</label>
      <select id='country' v-model="formValues.country">
        <option value=''>Select a country</option>
        <option value='india'>India</option>
        <option value='vietnam'>Vietnam</option>
        <option value='singapore'>singapore</option>
      </select>
    </div>

    <!-- multiple selection -->
    <div>
      <label for='location'>Location</label>
      <select id='location' multiple v-model="formValues.jobLocation">
        <option value='india'>India</option>
        <option value='vietnam'>Vietnam</option>
        <option value='singapore'>singapore</option>
      </select>
    </div>

    <!-- single checkbox -->
    <div>
      <input type='checkbox' id='remoteWork' v-model="formValues.remoteWork" true-value='yes' false-value='no'/>
      <label for='remoteWork'>Open to remote work</label>
    </div>

    <!-- multiple checkbox -->
    <div>
      <label>Skill Set</label>
      <input type='checkbox' id='html' value='html' v-model='formValues.skillSet'/>
      <label for='html'>HTML</label>
      <input type='checkbox' id='css' value='css' v-model='formValues.skillSet'/>
      <label for='css'>CSS</label>
      <input type='checkbox' id='JS' value='JS' v-model='formValues.skillSet'/>
      <label for='js'>JS</label>
    </div>

    <!-- radio button -->
    <div>
      <label>Years of Experience</label>
      <input
        type='radio'
        id='0-2'
        value='0-2'
        v-model='formValues.yearsOfExperience'
      />
      <label for="0-2">0-2</label>
      <input
        type='radio'
        id='3-5'
        value='3-5'
        v-model='formValues.yearsOfExperience'
      />
      <label for="3-5">3-5</label>
      <input
        type='radio'
        id='6-10'
        value='6-10'
        v-model='formValues.yearsOfExperience'
      />
      <label for="6-10">6-10</label>
    </div>

    <!-- submit button -->
    <div>
      <button @click="submitform">Submit</button>
    </div>


  </form>
  <div></div>
</template>

 
<script>
export default {
  name: 'App',
  data() {
    return{
      formValues: {
        name: '',
        profileSummary:'',
        country: '',
        jobLocation: [],
        remoteWork: 'no',
        skillSet: [],
        yearsOfExperience: '',
        age: null
      }
    }
  }, 
  methods: {
    submitForm(event){
      event.preventDefault() //prevent refresh
      console.log(this.formValues)
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
