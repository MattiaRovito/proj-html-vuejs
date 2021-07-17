<template>
    <header >

        <div class="d-flex justify-content-between p-3">
            <!-- logo -->
            <div class="p-2">
                <a href="#">
                    <img src="@/assets/img/logo-sidearea-1.png" alt="Logo">
                </a>
            </div>
            <!-- /logo -->
        

            <!-- utilizzato un v-for per ciclare un array all'interno di una nav -->
            <nav class="d-flex">
                <ul class="d-flex text-uppercase fw-bold">
                    <li v-for="(element, i) in menu" :key="i" class="m-3 underline"><a href="#">{{element}}</a>
                
                    </li>
                </ul>
                <div class="mx-2 p-1 mt-2">
                    <a href="#"><img src="@/assets/svg/svg-1.svg" alt="menu"></a>
                </div>
            
                
            </nav>
            <!-- /nav -->

        </div>

        <Jumbotron/>

    </header>
   
</template>
 
<script>
import Jumbotron from '@/components/Jumbotron.vue'
export default {
    name: 'Header',
    components: {
        Jumbotron
    },
    data (){
        return {
            menu : ['Home', 'Pages', 'Portfolio', 'Blog', 'Shop', 'Elements']
        }
       
    }
}
</script>

<style lang="scss" scoped>

//! ALZARE LA BARRA VICINO AL MENU + CAMBIARE I COLORI PER OGNI SINGOLA SEZIONE

// ul li:first-child
// {
//     content: "";
//     border-bottom: 3px solid rgb(34, 156, 34);
//     width: 100%;
//     // height: 3px;
//     // background-color: rgb(34, 156, 34);
//     display: block; 
// }


li
{
    font-size: 14px;

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