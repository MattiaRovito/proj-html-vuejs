<template>
<div>
<!--! VEDERE SEGNALIBRO SU FIREFOX PER LO SLIDER VUE-CLI -->
<!-- Usare carousel (vedere bootstrap+npm) -->

    
    
    
    <div class="d-flex">

        <!-- pulsante prev -->
        <div class="prev">
            <i class="fas fa-chevron-left"></i>
        </div>
        <!-- /pulsante prev -->
        
        
        <div>
            <div class="first-text">{{txtJ}} <strong class="fst-italic fw-bold">{{txtSJ}}</strong></div>
            <p>{{captionJ}}</p>
            <button class="btn text-uppercase rounded-0"><span class="filling">{{btnJ}}</span></button>
            
           

        </div>

        <img :src="require('@/assets/img/' + imgJ + '.png')" :alt="imgJ" class="w-75 jumbo">

        <img :src="require('@/assets/img/' + leafOne + '.png')" :alt="leafOne" class="position-absolute leaf_one"> 
        <img :src="require('@/assets/img/' + leafTwo + '.png')" :alt="leafTwo" class="position-absolute leaf_two">   
        <img :src="require('@/assets/img/' + leafThree + '.png')" :alt="leafThree" class="position-absolute leaf_three">
        <img :src="require('@/assets/img/' + leafFour + '.png')" :alt="leafFour" class="position-absolute leaf_four">
        <img :src="require('@/assets/img/' + leafFour + '.png')" :alt="leafFour" class="position-absolute leaf_fourth">

        <!-- pulsante next -->
        <div class="next">
            <i class="fas fa-chevron-right"></i>
        </div>
        <!-- /pulsante next -->

        



    </div>
        <!-- three points -->
        <div class="d-flex justify-content-center">
            <div class="point"></div>
            <div class="point"></div>
            <div class="point"></div>
        </div>
</div>
</template>

<script>
export default {
    name: 'Jumbotron',
    props: {
        imgJ: Image,
        txtJ: String,
        txtSJ: String,
        captionJ: String,
        btnJ: String,
        leafOne: Image,
        leafTwo: Image,
        leafThree: Image,
        leafFour: Image
    },
  


    
    
}
</script>

<style lang='scss' scoped>

.first-text
{
    font-size: 90px;
    padding: 150px 50px 0 300px;
    line-height: 1;
    font-weight: 100;
}


p
{
    color: #898988;
    font-size: 20px;
    padding: 20px 30px 0 300px;
}

.btn
{
    margin-left: 300px;
    margin-right: 415px;
    padding: 10px 35px;
    // margin: 20px;
    font-size: 14px;
    border: 3px solid #e1c0b0;
}

img
{
    margin-right: 80px;
    padding: 40px;
}

.prev, .next
{
    font-size: 20px;
    color: white;
    background-color: #e1c0b0;
    border-radius: 50%;
    padding: 0 10px 10px 10px;
    height: 30px;
    margin: 20px;
}

.prev
{
    position:absolute;
    left: 0;
    top: 400px;
}

.next
{
    position:absolute;
    right: 0;
    top: 400px;
}


.prev:hover, .next:hover
{
    transform: scale(1.2);
}

.jumbo
{
    padding: 20px;
}

.leaf_one{
    bottom: 236px;
    right: 800px;
}

.leaf_two{
    bottom: 160px;
    right: 720px;
}

.leaf_three{
    bottom: 180px;
    right: 85px;
}

.leaf_four{
    top: 212px;
    right: 800px;
}

.leaf_fourth{
    transform: rotate(90deg);
    top: 100px;
    right: 85px;
}


.point
{
    content:"";
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: #e1c0b0;
    margin: 20px 10px;

    &:hover
    {
        transform: scale(1.2);
    }
}

button:hover
{
    background-color: #e1c0b0;
    color: white;
}


</style>



