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
                <ul class="d-flex text-uppercase fw-bold dropdown">
                    <li v-for="(element, i) in menu" :key="i" class="m-3"><a href="#">{{element}}</a>
                        <ul class="dropdown-content">
                            <li v-for="(drop, i) in drops" :key='i'>{{drop}}</li>
                        </ul>
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
            :leafOne='jb.leafOne'
            :leafTwo='jb.leafTwo'
            :leafThree='jb.leafThree'
            :leafFour='jb.leafFour'
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
                    buttonJumbo: 'Read more',
                    leafOne: 'h-2-slider-img-12',
                    leafTwo: 'h-2-slider-img-13',
                    leafThree: 'h-2-slider-img-14',
                    leafFour: 'short-slider-rev-1-img-2'
                },
               
            ],
            drops : ['Main Home', 'Floating Portfolio', 'Portfolio Pinterest', 'Animated Slider', 'Portfolio Metro', ' Portfolio Gallery', ' Interactive Links', 'Split Slider Showcase', 'Portfolio Carousel', 'Landing']
        }
       
    }
}
</script>

<style lang="scss" scoped>





li
{
    font-size: 14px;
    position:relative;

    a::after
    {
    content: "";
    width: 0;
    height: 4px;
    background-color: rgba(34, 156, 34, 0.3);
    display: block;
    transition: width 0.5s;
    position:absolute;
    bottom: 6px;
    left: 0;
    }

    a:hover::after 
    {
    width: 100%;
    }

}


.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: fixed;
  right: 470px;
  background-color: #faf7f2;
  min-width: 250px;
  padding: 20px 18px;
  z-index: 1;
  font-size: 16px;

}

.dropdown:hover .dropdown-content {
  display: block;
}







</style>