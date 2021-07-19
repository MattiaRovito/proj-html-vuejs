<template>
    <header>

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
        <div>
            <Jumbotron 
            v-for="(jb, i) in jumbos" 
            :key="i" 
            :imgJ='jb.imgJumbo'
            :txtJ='jb.textJumbo'
            :txtSJ='jb.textStrongJumbo'
            :captionJ='jb.captionJumbo'
            :btnJ='jb.buttonJumbo'
            />
        </div>
        

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
            menu : ['Home', 'Pages', 'Portfolio', 'Blog', 'Shop', 'Elements'],
            // Se si crea un array di oggetti si possono passare tramite active le barre colorate   
            jumbos : [
                {
                    imgJumbo: 'h-2-slider-img-11',
                    textJumbo: 'Our new folio full of',
                    textStrongJumbo: 'joy', 
                    captionJumbo: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.',
                    buttonJumbo: 'Read more'
                },
                // {
                //     imgJumbo: 'h-2-slider-img-11',
                //     textJumbo: 'Our new folio full of',
                //     textStrongJumbo: 'joy', 
                //     captionJumbo: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.',
                //     buttonJumbo: 'Read more'
                // }
            ]
        }
       
    }
}
</script>

<style lang="scss" scoped>





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