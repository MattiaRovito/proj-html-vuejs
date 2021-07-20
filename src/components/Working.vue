<template>
  <div class="mt-3 ideas">
      <i :class="imgI" class="font-i"></i>
      <div class="p-3">
        <div class="h5">{{txtI}}</div>
        <span>{{idI}}</span>
      </div>
      
  </div>
</template>

<script>
export default {
    name: 'Working',
    props: {
        imgI: String,
        txtI: String,
        idI: String,
        colorI: String
    }
}
</script>

<style lang='scss' scoped>


.font-i
{
  font-size: 50px;
  padding:55px 60px;
  border-radius: 50%;
  background-color: #faf7f1;
  // opacity: 0;
  // transition: opacity 0.5s;
}

// .font-i:hover
// {
//   opacity: 1
// }


.h5
{
    margin-top: 55px;
}
span
{
    line-height: 1.8;
    color:#828282;
}

.font-i
{
  color: #badac9;
}


</style>