<template>
    <div>
        <div class="row">

       
        <Illustration class="col-4" v-for="(pic, i) in pics" :key='i'
            :img='pic.image'
            :txt='pic.text'
            :id='pic.id'
            />

        </div>

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
                
            ]                   
        }
    }
}
</script>

<style lang='scss' scoped>


</style>