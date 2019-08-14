<template>
   <div class="text-wrapper">
      <input type="text" :value='value' @input='textChage($event.target.value)'
      :placeholder="palceholder"
      :class="{'error-borer':errorMassge}"
      >
      <p v-if='validateData' class="error">{{errorMassge}}</p>
   </div>
</template>

<script>
export default {
    props:['value','palceholder','minLength'],
    data(){
        return{
            validateData :false
        }
    },
    computed:{
            errorMassge(){
                if(!this.validateData){
                    return ''
                }
                if(this.minLength && this.value.length<this.minLength){
                    return `Enter must be ${this.minLength} characters`
                }
                return ''
            }
    },
    methods:{
      textChage(e){
      //this.$emit('switchValue')
      this.$emit('input',e)
      this.validateData = true
  },
  validatadForm(){
      this.validateData = true;
  }
 }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style>

    .error{
        color: red;
        padding:0;
        margin: 0;
    }
    .error-borer{
        border: 1px solid red;
    }
</style>