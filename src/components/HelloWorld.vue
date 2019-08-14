<template>
  
   <div class="header">
      <div class="container">
          <div class="row">
              <div class="col-md-3 col-lg-3">
                 <a href="#">Logo</a>
              </div>
              <div class="col-md-9 col-lg-9">
                <transition name="fade" v-if="show">
                  <div class="navbarr">
                    <ul>
                      <li> <a href="">home</a> </li>
                      <li><a href="">work</a></li>
                      <li><a href="">protfolio</a></li>
                      <li><a href="">blog</a></li>
                      <li><a href="">about</a></li>
                      <li><a href="">servies</a></li>
                      <li><a href="">contact</a></li>
                    </ul>
                    <div class="cross" @click="show = false"><i class="fas fa-window-close"></i></div>
                </div>
                </transition>
                <div class="toggle" @click="show = !show"><i class="fas fa-bars"></i></div>
              </div>
          </div>
      </div>
       
    </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      show :false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}


.toggle {
  color: #fff;
  font-size: 20px;
  cursor: pointer;
  text-align: right;
}

.fade-enter-active,
.fade-leave-active{
  transition: margin-top 1s;
}
.fade-enter,
.fade-leave-to{
  margin-top:-555px;
}
.header {
    background: #ddd;
    height: 80px;
    line-height: 50px;
    position: relative;
}
.navbarr{
  position: fixed;
  background: #f00;
  height: 100%;
  width: 100%;
  text-align: center;
  left: 0;
  z-index: 2;
}
.navbarr ul li {
    font-size: 18px;
    color: #fff;
    text-transform: capitalize;
    padding-right: 41px;
}
</style>
