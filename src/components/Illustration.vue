<template>
    
    
    <div class="col-6">
            
    
            <div class="box">
                <img :src="img" :alt="img" class="immagini">
                <h2>{{txt}}</h2>
                <p class="fst-italic">{{id}}</p>
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

.immagini
{
    width: 50%;
}

.box
{
    border: 1px solid black;
    width: 100%;
}
</style>