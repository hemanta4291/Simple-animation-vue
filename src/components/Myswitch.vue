<template>
   <div class="switch-wrapper">
       <!-- <div class="s-wrapper" :class="{'on':SwitchValue,'off':!SwitchValue}" @click="switchChage">
           <div class="circle"></div>
       </div> -->

       <div class="s-wrapper" :class="{'on':value,'off':!value}" @click="switchChage">
           <div class="circle"></div>
       </div>
   </div>
</template>

<script>
export default {
    //props:['SwitchValue'],
    props:['value'],
  data () {
    return {
     
    }
  },
 methods:{
      switchChage(){
      //this.$emit('switchValue')
      this.$emit('input',!this.value)
  }
 }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
