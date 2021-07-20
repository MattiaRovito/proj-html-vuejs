<template>
  <div class="text-center position-relative">
      <div class="txt">Working <strong class="fst-italic">process</strong></div>

      <div class="row justify-content-center m-0 p-0" >

        <Working 
        class="col-2 m-0 p-0"
        v-for="(idea, i) in ideas" 
        :key='i'
        :imgI='idea.imgIdeas'
        :txtI='idea.textIdeas'
        :idI='idea.idIdeas'
        />
      </div>


      
      <div class="position-absolute top-50">
          <img src="@/assets/svg/svg-3.svg" alt="wave">
      </div>
        
    
  </div>
</template>

<script>
import Working from '@/components/Working.vue'
export default {
    name: 'Process',
    components: {
      Working
    },
    data(){
      return {
        ideas: [
          {
            imgIdeas: 'bi bi-lightbulb-fill',
            textIdeas: 'First theres an idea',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.'
          },
          {
            imgIdeas: 'bi bi-chat',
            textIdeas: 'Then we talk about',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.'
          },
          {
            imgIdeas: 'bi bi-cloud-fill',
            textIdeas: 'And we think about',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.'
          },
          {
            imgIdeas: 'bi bi-pencil',
            textIdeas: 'So we draw along',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.'
          },
        ]
      }
    }

}
</script>

<style lang="scss" scoped>
.txt
{
  padding-top: 150px;
  font-size: 65px;
  margin-bottom: 100px;
}



.position-absolute
{
  z-index: -3;
  left: 400px;
}


</style>