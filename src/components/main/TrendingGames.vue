

<script>
    // Js componente
    export default {
        name: 'TrendingGames',
        data() {
            return {
                games: [
                    {
                        name: "Assassin's Creed",
                        cover: 'protfolio1.png',
                        active: 'false'
                    },
                    {
                        name: 'Call Of Duty',
                        cover: 'protfolio2.png',
                        active: 'false'
                    },
                    {
                        name: 'Tomb Raider',
                        cover: 'protfolio3.png',
                        active: 'false'
                    },
                    {
                        name: 'Mortal Combat X',
                        cover: 'protfolio4.png',
                        active: 'false'
                    }
                ]
            }
        },
        methods: {
            
        }
    }
</script>


<template>
    <!-- html componente -->
    <section id="trending-games">
        <div class="container">
            <div class="col overview">
                <span class="sectionLittleTitle">Trending Games</span>
                <div class="title-and-buttons">
                    <h2 class="sectionTitle">Choose Who Is The Best<br>In World</h2>
                    <!-- buttons -->
                    <div class="arrow-buttons">
                        <button>
                            <svg class="svg-inline--fa fa-arrow-left-long" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="arrow-left-long" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M9.375 233.4l128-128c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25L109.3 224H480c17.69 0 32 14.31 32 32s-14.31 32-32 32H109.3l73.38 73.38c12.5 12.5 12.5 32.75 0 45.25c-12.49 12.49-32.74 12.51-45.25 0l-128-128C-3.125 266.1-3.125 245.9 9.375 233.4z"></path></svg>
                        </button>
                        <button>
                            <svg class="svg-inline--fa fa-arrow-right-long" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="arrow-right-long" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M502.6 278.6l-128 128c-12.51 12.51-32.76 12.49-45.25 0c-12.5-12.5-12.5-32.75 0-45.25L402.8 288H32C14.31 288 0 273.7 0 255.1S14.31 224 32 224h370.8l-73.38-73.38c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0l128 128C515.1 245.9 515.1 266.1 502.6 278.6z"></path></svg>
                        </button>
                    </div>
                </div>
                <div class="games">
                    <div v-for="(game, index) in games" :key="index" class="game">
                        <figure class="game-cover">
                            <img :src="`../../src/assets/img/${game.cover}`" :alt="game.name">
                            <span class="badge">New</span>
                        </figure>
                        <div class="game-info">
                            <div class="title-description">
                                <h3>{{ game.name }}</h3>
                                <p>Donec sollicitudin malesuada.</p>
                            </div>
                            <button>
                                <svg class="svg-inline--fa fa-play" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="play" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" data-fa-i2svg=""><path fill="currentColor" d="M361 215C375.3 223.8 384 239.3 384 256C384 272.7 375.3 288.2 361 296.1L73.03 472.1C58.21 482 39.66 482.4 24.52 473.9C9.377 465.4 0 449.4 0 432V80C0 62.64 9.377 46.63 24.52 38.13C39.66 29.64 58.21 29.99 73.03 39.04L361 215z"></path></svg>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
</template>


<style lang="scss" scoped>
    /* stile del componente */
    @use '../../assets/styles/partials/variables' as *;
    @use '../../assets/styles/partials/mixins' as *;

    #trending-games {
        background-color: $deep-blue;
        color: white;
        padding: 7rem 0;
        background-image: url('../../assets/img/protfolio-vector.png');
        @include bg-center-cover;

        .container {
            // border: 1px solid red;
    
            .overview {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                gap: 0.5rem;
    
                .title-and-buttons {
                    display: flex;
                    align-items: flex-end;
                    justify-content: space-between;
    
                    .arrow-buttons {
                        display: flex;
                        gap: 0.5rem;
                        button {
                            border: 0;
                            border-radius: 50%;
                            padding: 0.5rem;
                            display: flex;
                            align-items: center;
                            justify-content: center;
                            svg {
                                width: 20px;
                                aspect-ratio: 1;
                                padding: 0.2rem;
                            }
    
                            &:hover {
                                background-color: $full-green;
                                color: white;
                            }
                        }
                    }
                }

                .games {
                    @include d-flex-align-center;
                    gap: 0.5rem;
                    margin-top: 2rem;

                    > .game {
                        flex-basis: calc(100% / 4 - (1.5rem / 4));
                        display: flex;
                        flex-direction: column;
                        gap: 0.5rem;
                        background-color: #152257;

                        &:hover {
                            background-color: $light-green;

                            .game-info {
                                button {
                                    background-color: $dark-blue;

                                    svg {
                                        color: $light-green;
                                    }
                                }
                            }
                        }

                        .game-cover {
                            position: relative;

                            .badge {
                                position: absolute;
                                top: 0;
                                left: 0;
                                background-color: $light-green;
                                color: $dark-blue;
                                padding: 0.5rem 1rem;
                            }
                        }

                        .game-info {
                            @include d-flex-align-center;
                            justify-content: space-between;
                            padding: 1rem 0.5rem;

                            button {
                                color: $deep-blue;
                                background-color: $light-green;
                                border: 0;
                                height: 35px;
                                cursor: pointer;

                                aspect-ratio: 1;
                                @include d-flex-align-center;
                                justify-content: center;
                                border-radius: 50%;
                                padding: 0.5rem;

                                > svg {
                                    height: 100%;
                                    text-align: center;
                                }
                            }
                        }
                    }
                }
            }
        }
    }

    
</style>