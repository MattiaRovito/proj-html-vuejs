<template>
    
    
    <div>
                
        <!-- Il require permette di importare le immagini da una components all'altra. Indispensabile. -->

       
        

        <div class="position-relative">
            <img :src="require('@/assets/img/' + img + '.jpg')" :alt="img" class="w-100 image">

                 
            <div class="box">  
                <a href="#" class="text"><p>{{txt}}</p></a>
                <a href="#"><p class="fst-italic text-decoration-underline">{{id}}</p></a>
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
    width: 0%;
    opacity: 0;
    padding: 20px;
    transition: width .35s ease-in-out;

    .text
    {
        font-size: 28px;
    }
}

.position-relative:hover > .box
{
    width: 55%;
    opacity: 1;
}




</style>



