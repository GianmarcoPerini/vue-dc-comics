<template>
    <ul>
        <li v-for="el in dcComics" :key="el"><a :href="el.url">{{el.type}}</a></li>
    </ul>
</template>

<script>
export default {
    name: 'DCcomics',
    data: function(){
        return {
            dcComics: [
                {
                    type: 'Characters',
                    url: '#',
                },
                {
                    type: 'Comics',
                    url: '#',
                },
                {
                    type: 'Movies',
                    url: '#',
                },
                {
                    type: 'TV',
                    url: '#',
                },
                {
                    type: 'Games',
                    url: '#',
                },
                {
                    type: 'Videos',
                    url: '#',
                },
                {
                    type: 'News',
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