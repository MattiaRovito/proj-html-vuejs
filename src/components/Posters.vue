<template>
  <div class="position-relative">
  
   
    <div class="margin">
      <div class="box-position">
        <div class="box-top fst-italic fw-bold">{{dayP}}</div>
        <div class="box-bottom text-uppercase">{{monthP}}</div>
      </div>
      
      <img :src="require('@/assets/img/' + imgP + '.jpg')" :alt="imgP" class="w-100 box-img">
    </div>
    
    <div class="h4 mt-3"><a href="#">{{txtP}}</a></div>
    <span class="fst-italic">{{idP}}</span>
  </div>
</template>

<script>
export default {
    name: 'Posters',
    props: {
      imgP: Image,
      txtP: String,
      idP: String,
      dayP: Number,
      monthP: String
    }
}
</script>

<style lang="scss" scoped>

.box-position
{
  position:absolute;
  top: 130px;
  left: 30px;
  z-index: 99;
}

.box-top
{
  font-size: 26px;
  background-color: #c0e1cf;
  width: 100%;
  padding: 4px 15px;
}
.box-bottom
{
  font-size: 14px;
  background-color: #f3d0c7;
  width: 100%;
  height: 38px;
  clip-path: polygon(0 0,100% 0,100% 100%,50% 70%,0 100%);
  padding: 3px 8px;
}
.margin
{
  margin-top: 150px;
}


img
{
  transition: transform 0.20s;
  &:hover
  {
    transform: scale(1.009);
  }
}



.h4
{
   a::after
    {
    content: "";
    width: 0;
    height: 3px;
    background-color: rgb(34, 156, 34);
    display: block;
    transition: width 0.5s;
    }

    a:hover::after 
    {
    width: 100%;
    }
}



</style>