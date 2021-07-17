<template>
    <div>
        <Illustration class="row" v-for="(pic, i) in pics" :key='i'
            :img='pic.image'
            :txt='pic.text'
            :id='pic.id'
            />

        <Process/>

        <Message/>

        <Posters/>
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
                    image : '../assets/img/h-2-port-img-1.jpg',
                    text: 'All these illustrations',
                    id: 'Illustration'

                },
                {
                    image : '../assets/img/h-2-port-img-2.jpg',
                    text: 'Type and Illustrations',
                    id: 'Illustration'
                },
                {
                    image : '../assets/img/h-2-port-img-3.jpg',
                    text: 'Draw and illustrate',
                    id: 'Illustration'
                },
                {
                    image : '../assets/img/h-2-port-img-4.jpg',
                    text: 'Illustrations of novels',
                    id: 'Illustration'
                },
                {
                    image : '../assets/img/h-2-port-img-5.jpg',
                    text: 'Too many illustrations',
                    id: 'Illustration'
                },
                {
                    image : '../assets/img/h-2-port-img-6.jpg',
                    text: 'Dreams are illustrations',
                    id: 'Illustration'
                }
                
            ]                   
        }
    }
}
</script>

<style lang='scss' scoped>


</style>