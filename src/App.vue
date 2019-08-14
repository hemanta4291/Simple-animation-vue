<template>
  <div id="app">
    
     <HelloWorld/>
     <div class="main-wrapper">
       <div class="container">
         <div class="row">
           <div class="col-lg-3 col-md-3">
              <div class="left-side">
                <ul>
                  <li><router-link to="/" exact>Switch</router-link></li>
                  <li><router-link to="/switch">text-input</router-link></li>
                </ul>
              </div>
           </div>
          <div class="col-lg-9 col-md-9">
             <div class="right-side">
               <router-view></router-view>
             </div>
          </div>
         </div>
       </div>
     </div>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>


