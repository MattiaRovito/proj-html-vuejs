<template>

    <div>

        <!-- <img :src="img" :alt="img" class="immagini"> -->
    
        <div class="box">
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
    width: 20%;
}
</style>