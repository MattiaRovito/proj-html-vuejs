<template>
  <div id="app">
    
      <div class="qode d-flex">
        <img src="@/assets/svg/svg-4.svg" alt="svg">
        <span class="text-uppercase related">Related</span>
      </div>
    

    <!-- <div class="shop d-flex">
      <img src="@/assets/svg/svg-9.svg" alt="svg">
      <span class="text-uppercase related">Buy Now</span>
    </div> -->
    

    <Header/>

    <Main/>

    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import '@/style/commons.scss';




.qode
{
  width: 2%;
  position:fixed;
  right: 80px;
  top: 170px;
  background-color: red;
  z-index: 1000;
}

.related
{
  line-height: 3;
  margin-left: 8px;
  font-size: 14px;
  
}




</style>
