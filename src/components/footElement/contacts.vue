<template>
    <div class="contacts">
        <div class="sign">
            <h2><a href="">SIGN-UP NOW!</a></h2>
        </div>

        <div class="social">
            <h2><a href="">FOLLOW US</a></h2>
            <a :href="el.alt" v-for="el in socials" :key="el"><img :src="require('../../assets/' + el.social)" :alt="el.alt"></a>
        </div>
    </div>
</template>

<script>
export default {
    name:'Foot',
    data: function(){
        return{
            socials: [
                {
                    social:'footer-facebook.png',
                    url:'#',
                    alt: '',
                },
                {
                    social:'footer-twitter.png',
                    url:'#',
                    alt: '',
                },
                {
                    social:'footer-youtube.png',
                    url:'#',
                    alt: '',
                },
                {
                    social:'footer-pinterest.png',
                    url:'#',
                    alt: '',
                },
                {
                    social:'footer-periscope.png',
                    url:'#',
                    alt: '',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../general.scss';

.contacts{
    background-color: #303030;
    color: white;
    padding: 40px 0;
    display: flex;
    justify-content: space-between;

    .sign{
        border: 2px solid $primary;
        display: inline-block;
        padding: 10px 20px;
        margin-left: 100px;

        a{
            color: white;
            text-decoration: none;
        }
    }

.social{
    display: flex;
    align-items: center;
    margin-right: 100px;

    h2 a{
        color: $primary;
        margin-right: 30px;
        text-decoration: none;

    }

    img{
        margin-right: 10px;
    }
}

}
</style>