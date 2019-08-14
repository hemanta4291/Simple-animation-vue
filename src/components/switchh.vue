<template>
   <div class="switch">
       <h1>switch</h1>
       <hr>
      <!-- <Myswitch :switch-value='SwitchValue' @switchValue="SwitchValue = !SwitchValue" /> -->
      <Myswitch v-model="SwitchValue"/>
   </div>
</template>

<script>

import Myswitch from './Myswitch'

export default {
  data(){
    return {
      SwitchValue: true
    }
  },
  components:{
    Myswitch
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
