<template>
    <ul>
        <li v-for="el in dcComics" :key="el"><a :href="el.url">{{el.type}}</a></li>
    </ul>
</template>

<script>
export default {
    name: 'DC',
    data: function(){
        return{
            dcComics: [
                {
                    type: 'Terms of use ',
                    url: '#',
                },
                {
                    type: 'Privacy Policy (new)',
                    url: '#',
                },
                {
                    type: 'Add Choise',
                    url: '#',
                },
                {
                    type: 'Advertising',
                    url: '#',
                },
                {
                    type: 'Jobs',
                    url: '#',
                },
                {
                    type: 'Subscriptions',
                    url: '#',
                },
                {
                    type: 'Talent Workshop',
                    url: '#',
                },
                {
                    type: 'CPSC Certificates',
                    url: '#',
                },
                {
                    type: 'Rating',
                    url: '#',
                },
                {
                    type: 'Shop Helps ',
                    url: '#',
                },
                {
                    type: 'Contact Us',
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