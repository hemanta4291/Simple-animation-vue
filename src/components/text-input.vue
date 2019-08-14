<template>
  
   <div class="textinput">
     <h1>Text Input</h1>
       <hr>
       <text-input v-model='text' palceholder="Enter Username"
       min-length = "5" ref="username"/>
       <br>
       <button @click="submitMethod">submit</button>

       <p v-if='submitData'>result: {{text}}</p>

   </div>
</template>

<script>
import TextInput from './my-input-text'
export default {
  data () {
    return {
      text : '',
      submitData:false
    }
  },
  methods:{
      submitMethod(){
        this.$refs.username.validatadForm();
        if(this.$refs.username.errorMassge){
          return ''
        }
        this.submitData = true;
      }
  },
  components:{
    TextInput
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
