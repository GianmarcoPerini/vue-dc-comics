<template>
    <div class="card">
        <img :src="image" alt="">
        <p>{{title}}</p>
    </div>
</template>

<script>



export default {
    name: 'Jumbo',
    props: {
        title: String,
        image: String,
    }
    


}
</script>

<style lang="scss" >
    .card{
        margin: 20px 10px;
        width: calc(100% /6 - 20px);
        transition: transform 100ms ease-in-out;
        
        img{
            width: 100%;
        }

        p{
            font-size: .85rem;
            color: white;
            text-transform: uppercase;
            margin-top: 9px;
        }

        &:hover{
            transform: scale(1.1);
        }

    }
</style>