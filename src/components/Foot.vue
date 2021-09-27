<template>
    <footer>
        <div class="foot-wrap">
            <div>
                <nav>
                    <h2>DC CCOMICS</h2>
                    <DCcomics /> 
                </nav>

                <nav class="mt-1">
                    <h2>SHOP</h2>
                    <Shop />
                </nav>
            </div>
            <div>
                <nav class="m-1">
                    <h2>DC</h2>
                    <DC />
                </nav>
            </div>
            <div>
                <nav>
                    <h2>SITE</h2>
                    <site />
                </nav>
            </div>


            <img src="../assets/dc-logo.png" alt="">
        </div>


        <contacts />
        
    </footer>
</template>

<script>
import DCcomics from './footElement/DCcomics.vue'
import Shop from './footElement/shop.vue'
import DC from './footElement/DC.vue'
import Site from './footElement/site.vue'
import Contacts from './footElement/contacts.vue'

export default {
    name: 'Footer',
    components: {
        DCcomics,
        Shop,
        DC,
        Site,
        Contacts,
    }

}
</script>

<style lang="scss" scoped>
@import './general.scss';

.mt-1{
    margin-top: 15px;
}

.m-1{
    margin-left: 50px;
    margin-right: 50px;
}

.foot-wrap{

    background-image: url(../assets/footer-bg.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    overflow: hidden;
    display: flex;
    padding: 50px 0 50px 100px;
    
    nav{
        z-index: 1;

        h2{
            color: white;
            margin-bottom: 20px;
        }

        ul{
            list-style: none;
            font-size: .8rem;
        }
    }


    img{
        position: absolute;
        top: -90px;
        right: 50px;
        height: 160%;
        transform: rotate(-25deg);
        opacity: .5;
        mix-blend-mode: lighten;
        z-index: 0;
        pointer-events: none;
    }
}

</style>