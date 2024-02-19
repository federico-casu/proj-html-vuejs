

<script>
    // Js componente

    import { store } from '../../store';
 
    export default {
        name: 'TopPlayers',
        data() {
            return {
               store 
            }
        },
        methods: {
            
        }
    }
</script>


<template>
    <!-- html componente -->
    <div class="">
        <ul>
            <li v-for="(player, index) in store.playersImages" :key="index">
                <img :src="`../../src/assets/img/${player}.png`" alt="">
            </li>
        </ul>
    </div>
    
</template>


<style lang="scss" scoped>
    /* stile del componente */
    @use '../../assets/styles/partials/mixins' as *;
    @use '../../assets/styles/partials/variables' as *;

    div {
        // border: 1px solid red;
        background-color: $deep-blue;
        border-radius: 10px;
        width: 100%;
        // position: absolute;
        // top: -10%;

        ul {
            @include d-flex-align-center;
            justify-content: space-between;
            color: white;
            padding: 1rem;

            li {
                list-style-type: none;
                @include d-flex-align-center;
                justify-content: center;

                img {
                    width: 80%;
                }
            }
        }
    }
    
</style>