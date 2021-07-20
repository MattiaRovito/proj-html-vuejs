<template>
  <div id="app">
    
      <div class="qode position-fixed p-3">
        
         
            <img src="@/assets/svg/svg-4.svg" alt="svg" class="w-img me-2">
          
            <span class="text-uppercase related">Related</span>
            
          
      </div>
    

    <div class="shop d-flex position-fixed">

          <img src="@/assets/svg/svg-6.svg" alt="svg">
      
          <span class="text-uppercase buy">Buy Now</span>

      
    </div>
    

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
  },
  data(){
    return {
      informations: [
        {
          
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import '@/style/commons.scss';


.qode
{
  top: 170px;
  background-color: #ef2853;
}

.shop
{
  top: 250px;
  background-color: white;
  padding: 15px 13px;
  margin-left: 5px;
}


.qode, .shop
{
  right: -80px;
  z-index: 1000;
  width: 10%;
  height: 10%;
  cursor: pointer;
}


.w-img
{
  width: 13%;
}


.related
{
  font-size: 12px;
  color: white;
}

.buy
{
  font-size: 12px;
  padding: 5px;
}



</style>
