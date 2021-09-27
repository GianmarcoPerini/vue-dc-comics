<template>
    <footer>
        <div class="foot-block">
            <div class="foot-voices" v-for="(el, i) in footerMenu" :key="i">
                    <h3>{{el.title}}</h3>
                    <p v-for="el in el.components" :key="el">{{el}}</p>
            </div>
        </div>

        <img src="../assets/dc-logo.png" alt="">

    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data: function(){
        return {
            footerMenu: [
                {
                    title: 'DC COMICS',
                    components: ['Characters','Comics','Movies','TV','Games','Videos','News']
                },
                {
                    title: 'SHOP',
                    components: ['Shop DC','Shop DC Collectibles']
                },
                {
                    title: 'DC',
                    components: ['Terms Of Us','Privacy police (New)','Add Choise','Advertising','Jobs','Subscriptions','Talente Workshop','CPSC Certificates','Ratings','Shop Help','Contacts']
                },
                {
                    title: 'SITE',
                    components: ['DC','MAD Magazine','DC Kids','DC Universe','DC Power Visa']
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import './general.scss';

footer{

    background-image: url(../assets/footer-bg.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    overflow: hidden;
    padding-left: 40px;
    height: 400px;
    display: flex;
    align-items: center;

    img{
        position: absolute;
        top: -90px;
        right: 50px;
        height: 160%;
        transform: rotate(-25deg);
        opacity: .5;
        mix-blend-mode: lighten;
        z-index: 0;
    }

    .foot-block{
        display: flex;
        flex-wrap: wrap;
        flex-direction: column;
        align-items: flex-start;
        height: 80%;
        width: max-content;

        .foot-voices{
            padding: 30px;
            z-index: 1;
        
                h3{
                    margin-bottom: 10px;
                    color: white;
                    font-size: 1.4rem;
                }
                
                p{
                    color: $footLinks;
                    font-size: .7em;

                        &:hover{
                            color: white;
                            cursor: pointer;
                            text-decoration: underline;
                        }
                }
        }
    }


}



</style>