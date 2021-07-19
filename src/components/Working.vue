<template>
  <div class="mt-3 ideas">
      <i :class="imgI" class="font-i"></i>
      <div>{{txtI}}</div>
      <div>{{idI}}</div>
  </div>
</template>

<script>
export default {
    name: 'Working',
    props: {
        imgI: String,
        txtI: String,
        idI: String
    }
}
</script>

<style lang='scss' scoped>


.font-i
{
  font-size: 50px;
  padding: 60px;
  border-radius: 50%;
  background-color: #faf7f1;
}

.font-i:first-child
{
  color: #badac9;
  transform: scaleX(-1); 
  -webkit-transform: scaleX(-1); 
  -moz-transform: scaleX(-1); 
  -ms-transform: scaleX(-1); 
  -o-transform: scaleX(-1); 
}

.font-i:nth-child(2)
{
  color: #f8d12d;
}

.font-i:nth-child(3)
{
  color: #80465f;
}

.font-i:last-child
{
  color: #eb6950;
}
</style>