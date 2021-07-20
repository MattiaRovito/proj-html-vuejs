<template>
    <div class="bg-image">
        <div class="container text-center">
            <div class="txt">Want to work with us? Send us <strong class="fst-italic">a message!</strong></div>
            <p class="mt-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore pariatur, nemo dolor, porro accusantium, aut autem esse doloremque repellendus beatae repellat exercitationem quibusdam qui labore dolores possimus saepe at iusto.</p>
            <button class="btn text-uppercase rounded-0"><span>contact</span></button>
        </div>
    </div>
  
</template>

<script>
export default {
    name: 'Message',
}
</script>

<style lang="scss" scoped>
.bg-image
{
    background-image: url('../assets/img/h-2-background-1.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 529px;
    margin-top: 180px;
}

.container
{
    .txt
    {
        padding-top: 150px;
        font-size: 65px;
    }
    p
    {
        color: #898988;
        font-size: 20px;
    }
    button
    {
        padding: 15px 40px;
        margin: 20px;
        font-size: 14px;
        color: black;
        background-color: #d8f0e3;
        span
        {
            margin: 0 20px;
        }

        &:hover
        {
            background-color: #e1c0b0;
            color: white;
        }
    }

}

</style>