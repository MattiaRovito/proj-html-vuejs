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
            <div class="btn-padding">
                <button class="btn text-uppercase rounded-0"><span>{{btnJ}}</span></button>
            </div>
           

        </div>

        <img :src="require('@/assets/img/' + imgJ + '.png')" :alt="imgJ" class="w-75">
        <!-- LE FOGLIE LE INSERISCO DIRETTAMENTE QUI PER POSIZIONARLE CON I POSITION ABSOLUTE -->

        <!-- pulsante next -->
        <div class="next">
            <i class="fas fa-chevron-right"></i>
        </div>
        <!-- /pulsante next -->
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
        btnJ: String
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
.btn-padding
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

</style>