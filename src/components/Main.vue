<template>
    <div>
        <div class="row m-0 p-0">

            <Illustration 
            class="col-4 p-0 m-0" 
            v-for="(pic, i) in pics" 
            :key='i'
            :img='pic.image'
            :txt='pic.text'
            :id='pic.id'
            />
        

        </div>

        <Process/>

        <Message/>

        <div class="row justify-content-center m-0">

            <Posters
            class="col-3"
            v-for="(poster,i) in posters" 
            :key="i"
            :imgP="poster.imgPos"
            :txtP="poster.textPos"
            :idP="poster.idPos"
            :dayP="poster.dayPos"
            :monthP="poster.monthPos"/>

        </div>
    </div>
   
</template>

<script>
import Illustration from '@/components/Illustration.vue'
import Process from '@/components/Process.vue'
import Message from '@/components/Message.vue'
import Posters from '@/components/Posters.vue'

export default {
    name: "Main",
    components:{
        Illustration,
        Process,
        Message,
        Posters
    },
    data(){
        return {
            pics : [
                {
                    image : 'h-2-port-img-1',
                    text: 'All these illustrations',
                    id: 'Illustration'

                },
                {
                    image : 'h-2-port-img-2',
                    text: 'Type and Illustrations',
                    id: 'Illustration'
                },
                {
                    image : 'h-2-port-img-3',
                    text: 'Draw and illustrate',
                    id: 'Illustration'
                },
                {
                    image : 'h-2-port-img-4',
                    text: 'Illustrations of novels',
                    id: 'Illustration'
                },
                {
                    image : 'h-2-port-img-5',
                    text: 'Too many illustrations',
                    id: 'Illustration'
                },
                {
                    image : 'h-2-port-img-6',
                    text: 'Dreams are illustrations',
                    id: 'Illustration'
                }
                
            ],
            posters: [
                {
                    imgPos: 'h-2-blog-img-1',
                    textPos: 'This way, loves: a detailed guide through new design',
                    idPos: 'By Emily Fields',
                    dayPos: '07',
                    monthPos: "May '19"
                },
                {
                    imgPos: 'h-2-blog-img-2',
                    textPos: 'I try to give people a different way of looking art',
                    idPos: 'By Emily Fields',
                    dayPos: '07',
                    monthPos: "May '19"
                },
                {
                    imgPos: 'h-2-blog-img-3',
                    textPos: 'Introduce Richard Laperrière of those amazing features',
                    idPos: 'By Emily Fields',
                    dayPos: '07',
                    monthPos: "May '19"
                },
            ]                   
        }
    }
}
</script>

<style lang='scss' scoped>


</style>