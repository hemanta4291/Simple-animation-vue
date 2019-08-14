<template>
   <div class="switch">
       <h1>switch</h1>
       <hr>
      <!-- <Myswitch :switch-value='SwitchValue' @switchValue="SwitchValue = !SwitchValue" /> -->
      <Myswitch v-model="SwitchValue"/>
       <Myswitch v-model="SwitchValue1"/>
        <Myswitch v-model="SwitchValue2"/>
   </div>
</template>

<script>

import Myswitch from './Myswitch'

export default {
  data(){
    return {
      SwitchValue: true,
       SwitchValue1: true,
        SwitchValue2: true
    }
  },
  components:{
    Myswitch
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
