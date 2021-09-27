<template>
    <main>
        <section class="cards">
            <Card v-for="game in gamesDC" :key="game" :title="game.series" :image="game.thumb" />
        </section>
        <Merch />
    </main>
</template>

<script>
import Merch from './mainElement/Merch.vue';
import Card from './mainElement/Card.vue';
import gamesDC from '../gamesDC.js';


export default {
    name: 'Main',
    components: {
        Merch,
        Card,
    },

    data: function(){
        return {
            gamesDC,
        }
    }
}
</script>

<style lang="scss" scoped>
@import './general.scss';

main{
    background-color: #1c1c1c;
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
