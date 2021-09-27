<template>
    <main>
        <jumboImg />
        <section class="cards">
            <Card v-for="game in gamesDC" :key="game" :title="game.series" :image="game.thumb" />
        </section>
        <button>LOAD MORE</button>
        
        <Merch />
    </main>
</template>

<script>
import Merch from './mainElement/Merch.vue';
import Card from './mainElement/Card.vue';
import gamesDC from '../gamesDC.js';
import jumboImg from './mainElement/jumboImg.vue'


export default {
    name: 'Main',
    components: {
        Merch,
        Card,
        jumboImg,
    },

    data: function(){
        return {
            gamesDC,
            jumboImg,
        }
    }
}
</script>

<style lang="scss">
@import './general.scss';

main{
    background-color: #1c1c1c;

    button{
        margin: 0 auto 30px;
        display: block;
        padding: 6px 70px;
        font-weight: bold;
        background-color: $primary;
        color: white;
        border-radius: 2px;
        border: none;
        cursor: pointer;
        transition: transform 50ms ease-in-out;

        &:hover{
            transform: scale(1.05);
        }
    }
}
.cards{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    width: 80%;
    margin: 0 auto;
    padding: 30px 0;
}

</style>
