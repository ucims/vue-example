<template>
  <div class="hello">
   <div class="holder">
     <ul>
       <li v-for="(data, index) in skills" :key="index">{{index}} . {{ data.skill}}</li>
     </ul>
     <p v-if="skills.length >= 1">You have more than 1 skill</p>
     <p v-else>You have less than or equal to 1 skill</p>
     <div v-bind:class="{ alert: showAlert, 'another-class' : showClass }"></div>
     <div v-bind:class="alertObject"></div>
   </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data(){
    return{
     skills: [
       {"skill" : "Vue.js"},
       {"skill" : "nothing"},
       {"skill" : "nothing"}
     ],
     showAlert : true,
     showClass : true,
     alertObject : {
       alert : true
     }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./skills.css" scoped>

</style>
