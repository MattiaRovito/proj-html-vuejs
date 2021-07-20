<template>
  <footer>
      <div class="container text-center">
        <nav>
          <ul class="row p-3">
            <li class="col-3 mb-2"><img src="@/assets/img/logo-sidearea-1.png" alt="logo"></li>
            <li class="col-3">maree.qode@gmail.com</li>
            <li class="col-3">Avenue d'Auderghem 10</li>
            <li class="col-3">Stay in touch with us</li>
            <li class="col-3">Let's Get Creative</li>
            <li class="col-3">+44645 321 789</li>
            <li class="col-3">1040 Brussels, Belgium</li>
            <li class="col-3 d-flex"><Social v-for="(social, i) in socials" :key="i" :social='social'/></li>
          </ul>
        </nav>
       
          
      </div>
  </footer>
</template>

<script>
import Social from '@/components/Social.vue'
export default {
name: 'Footer',
components:{
  Social
},
data(){
  return {
    socials: ['fab fa-twitter','fab fa-pinterest-p','fab fa-facebook-f','fab fa-linkedin-in']
  }
}
}
</script>

<style lang='scss' scoped>
footer
{
    height: 228px;
    margin-top: 150px;
    background-color: #c0e1cf;
    padding: 80px 100px;


}


</style>