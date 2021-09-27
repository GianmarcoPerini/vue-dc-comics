<template>
    <section class="merch">
        <div class="box-merch"
            v-for="(el, index) in merch"
            :key="index"   
            @click="getIndex(index)"
            :class="(count == index) ? 'active' : '' ">

            <div class="img-merch">
                <img :src="require('../../assets/' + el.url) " :alt="el.date">
                <p>{{el.type}}</p>
            </div>
            
            
        </div>

    </section>
</template>

<script>
export default {
    name:'Merch',
    data: function() {
        return{
            merch: [
                { type: 'DIGITAL COMICS', url: 'buy-comics-digital-comics.png', alt: 'dc comics logo telefono' },
                { type: 'DC MERCHANDISE', url: 'buy-comics-merchandise.png', alt: 'dc comics t-shirt' },
                { type: 'SUBSCRIPTION', url: 'buy-comics-shop-locator.png', alt: 'dc comics trova il negozio pù vicino' },
                { type: 'COMIC SHOP LOCATOR', url: 'buy-comics-subscriptions.png', alt: 'dc comics sottoscrivi un abbonamento' },
                { type: 'DC POWER VISA', url: 'buy-dc-power-visa.svg', alt: 'visa carta di credito' },
            ],

            count: 0,
        }
    },

    methods:{
        getIndex: function(index){
            this.count = index
            console.log(index);
        }
    }
}
</script>

<style lang="scss" scoped>

@import '../general.scss';


.merch{
    padding: 20px 0;
    background-color: $primary;
    display: flex;
    justify-content: center;
    




    .box-merch{
        display: flex;
        align-items: center;
        font-size: 1rem;
        width: 100%;
        padding: 20px;
        border-radius: 20px;
        border: 3px solid transparent;
        transition: all 200ms ease-in-out;
        cursor: pointer;
        margin-left: 5px;

        .img-merch{
            color: white;
            height: 40px;
            display: flex;
            align-items: center;

            p{
                margin-left: 20px;
                font-size: .8rem;
            }

            img{
                height: 100%;
            }
        }

        &:hover{
            border: 3px solid white;
        }


    }
}

.active{
    border: 3px solid white !important;
}
</style>