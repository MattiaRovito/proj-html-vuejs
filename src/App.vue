<template>
  <div id="app">
    
      <div class="qode position-fixed p-2 shadow">
        
         
            <img src="@/assets/svg/svg-4.svg" alt="svg" class="w-img">
          
            <span class="text-uppercase related fw-bold ms-2">Related</span>

                    
          
      </div>
    

    <div class="shop position-fixed p-2 shadow">
          <a href="https://themeforest.net/"><img src="@/assets/svg/svg-6.svg" alt="svg" class="w-shop"></a>

          <a href="https://themeforest.net/"><span class="text-uppercase buy fw-bold ms-2">Buy Now</span></a>
      
          
      
    </div>


    <div class="arrow-back position-fixed">
        <a href="#top"><img src="@/assets/svg/svg-2.svg" alt="svg" class="w-100"></a>
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
  top: 220px;
  background-color: white;
  margin-left: 5px;
}


.qode, .shop
{
  right: -80px;
  z-index: 1000;
  width: 10%;
  height: 4%;
  cursor: pointer;
}


.w-img
{
  width: 13%;
}

.w-shop
{
  width: 9%;
}


.related, .buy
{
  font-size: 10px;
}


// .box-related
// {
//   display: none;
//   width: 20%;
//   height: 400px;
//   background-color: red;
// }

.related
{
  color: white;

  // &:active + .box-related
  // {
  //   display: block;
  // }
}


.arrow-back
{
  background-color: #c0e1cf;
  padding: 15px;
  width: 50px;
  height: 50px;
  bottom: 30px;
  right: 30px;
  z-index: 1000;
}




</style>
