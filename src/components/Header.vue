<template>
    <header class="d-flex justify-content-between p-3">
        <div class="p-2">
            <img src="@/assets/img/logo-sidearea-1.png" alt="Logo">
        </div>
        
        <div class="d-flex">
            <ul class="d-flex text-uppercase fw-bold">
                <li v-for="(element, i) in menu" :key="i" class="m-3"><a href="#">{{element}}</a>
               
                </li>
            </ul>
            <div class="mx-2 p-1 mt-2">
                <a href="#"><img src="@/assets/svg/svg-1.svg" alt="menu"></a>
            </div>
           
            
        </div>
      
    </header>
</template>
 
<script>
export default {
    name: 'Header',
    data (){
        return {
            menu : ['Home', 'Pages', 'Portfolio', 'Blog', 'Shop', 'Elements']
        }
       
    }
}
</script>

<style lang="scss">

li
{
    font-size: 14px;
}






</style>