<template>
    <div>
        <Illustration v-for="(pic, i) in pics" :key='i'
            :img='pic.image'
            :txt='pic.text'
            :id='pic.id'
            />
    </div>
   
</template>

<script>
import Illustration from '@/components/Illustration.vue'
export default {
    name: "Main",
    components:{
         Illustration
    },
    data(){
        return {
            pics : [
                {
                    image : '@/assets/img/h-2-port-img-1.png',
                    text: 'All these illustrations',
                    id: 'Illustration'

                },
                {
                    image : '@/assets/img/h-2-port-img-2.png',
                    text: 'Type and Illustrations',
                    id: 'Illustration'
                },
                {
                    image : '@/assets/img/h-2-port-img-3.png',
                    text: 'Draw and illustrate',
                    id: 'Illustration'
                },
                {
                    image : '@/assets/img/h-2-port-img-4.png',
                    text: 'Illustrations of novels',
                    id: 'Illustration'
                },
                {
                    image : '@/assets/img/h-2-port-img-5.png',
                    text: 'Too many illustrations',
                    id: 'Illustration'
                },
                {
                    image : '@/assets/img/h-2-port-img-6.png',
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