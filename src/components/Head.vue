<template>

    <header> 
        
        <img src="../assets/dc-logo.png" alt="DC Logo">
        <nav>
            <ul>
                <li v-for="(link, index) in links" :key="index" @click="activeMenu(index, link)" :class="(count == index) ? 'active' : '' ">{{link.text}}</li>
            </ul>
        </nav>        
    </header>

</template>

<script>
export default {
    name: 'Head',
    data: function() {
        return {
            count: 0,

            links: [
                { text: 'CHARACTERS',isActive: false, },
                { text: 'COMICS',isActive: false, },
                { text: 'MOVIES',isActive: false, },
                { text: 'TV',isActive: false, },
                { text: 'GAMES',isActive: false, },
                { text: 'COLLECTIBLES',isActive: false, },
                { text: 'VIDEOS',isActive: false, },
                { text: 'FANS',isActive: false, },
                { text: 'NEWS',isActive: false, },
                { text: 'SHOP',isActive: false, },
            ],

            

        }

        


    },

                methods: {

                activeMenu: function(index, link){
                    this.count = index
                    link.isActive = !link.isActive
                }

            }

}
</script>

<style lang="scss" scoped>
@import './general.scss';

header{
    display: flex;
    width: 100%;
    justify-content: space-between;
    padding-left: 100px;
    padding-right: 100px;
    align-items: center;
    margin-top: 30px ;
    
    img{
        height: 100%;
    }

    ul{
        list-style: none;

        li{
            vertical-align: middle;
            color: $navLinks;
            padding: 60px 0;
            margin: 0 10px;
            font-weight: bold;
            display: inline-block;
            border-bottom: 5px solid transparent;
            cursor: pointer;
            transition: all 150ms ease-in-out;

            &:hover{
                border-bottom: 5px solid $primary;
            }
        }
    }
}

    .active{
        border-bottom: 5px solid $primary;
    }
    

</style>
