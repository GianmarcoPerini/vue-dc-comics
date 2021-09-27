<template>
    <ul>
        <li v-for="el in dcComics" :key="el"><a :href="el.url">{{el.type}}</a></li>
    </ul>
</template>

<script>
export default {
name: 'Site',
    data: function(){
        return{
            dcComics: [
                {
                    type: 'DC',
                    url: '#',
                },
                {
                    type: 'MAD Magazine',
                    url: '#',
                },
                {
                    type: 'DC Kids',
                    url: '#',
                },
                {
                    type: 'DC Universe',
                    url: '#',
                },
                {
                    type: 'DC Power Visa',
                    url: '#',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

li {
    margin-top: 5px;

    a{
    color: rgb(175, 175, 175);
    text-decoration: none;

        &:hover{
        color: rgb(224, 224, 224);
        }
    }
}

</style>