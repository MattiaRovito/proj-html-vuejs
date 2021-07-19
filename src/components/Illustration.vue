<template>
    
    
    <div>
                
        <!-- Il require permette di importare le immagini da una components all'altra. Indispensabile. -->

        <!-- Chiedere perché si è formata la barra orizzontale + eliminare margine tra le pics -->
        

        <div class="position-relative">
            <img :src="require('@/assets/img/' + img + '.jpg')" :alt="img" class="w-100 image">

                
            <div class="box">  
                <a href="#" class="text"><p>{{txt}}</p></a>
                <a href="#"><p class="fst-italic">{{id}}</p></a>
            </div>

        </div>
    
        
  

    </div>
    

      
      
 
</template>

<script>
export default {
    name: 'Illustration',
    props : {
        img: Image,
        txt: String,
        id: String
    },
    data(){
        return {
        
        }
    }
    
}
</script>

<style lang='scss' scoped>



.box
{
    position: absolute;
    z-index: 10;
    left: 0;
    top: 300px;
    background-color: white;
    width: 55%;
    padding: 20px;

    .text
    {
        font-size: 28px;
    }
}
</style>