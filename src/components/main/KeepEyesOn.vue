

<script>
    // Js componente
    export default {
        name: 'KeepEyesOn',
        data() {
            return {
                players: [
                    {
                        name: 'Ninja Warrior Gaming',
                        image: '1.png'
                    },
                    {
                        name: 'Witch Gaming',
                        image: '5.png'
                    },
                    {
                        name: 'SkullG Gaming',
                        image: '3.png'
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
                <span class="sectionLittleTitle">Upcoming Match</span>
                <div class="title-and-buttons">
                    <h2 class="sectionTitle">Keep Eyes & Manage<br>upcoming Battle</h2>
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
                <div class="players">
                    <div v-for="(player, index) in players" :key="index" class="player">
                        <figure class="player-image">
                            <img :src="`../../src/assets/img/${player.image}`" :alt="player.name">
                        </figure>
                        <div class="game-info">
                            <div class="title-description">
                                <h3>{{ player.name }}</h3>
                                <div class="buttons">
                                    <button id="youtube">
                                        <svg class="svg-inline--fa fa-youtube" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="youtube" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg=""><path fill="currentColor" d="M549.7 124.1c-6.281-23.65-24.79-42.28-48.28-48.6C458.8 64 288 64 288 64S117.2 64 74.63 75.49c-23.5 6.322-42 24.95-48.28 48.6-11.41 42.87-11.41 132.3-11.41 132.3s0 89.44 11.41 132.3c6.281 23.65 24.79 41.5 48.28 47.82C117.2 448 288 448 288 448s170.8 0 213.4-11.49c23.5-6.321 42-24.17 48.28-47.82 11.41-42.87 11.41-132.3 11.41-132.3s0-89.44-11.41-132.3zm-317.5 213.5V175.2l142.7 81.21-142.7 81.2z"></path></svg>
                                    </button>
                                    
                                    <button id="chat">
                                        <svg class="svg-inline--fa fa-message" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="message" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M511.1 63.1v287.1c0 35.25-28.75 63.1-64 63.1h-144l-124.9 93.68c-7.875 5.75-19.12 .0497-19.12-9.7v-83.98h-96c-35.25 0-64-28.75-64-63.1V63.1c0-35.25 28.75-63.1 64-63.1h384C483.2 0 511.1 28.75 511.1 63.1z"></path></svg>
                                    </button>
                                </div>
                                <span>9.45</span>
                                <p>1st November, 2022</p>
                                <button id="view-more">View More</button>
                            </div>
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
        // background-color: $deep-blue;
        color: white;
        padding: 6rem 0;
        background-image: url('../../assets/img/v-bg.png');
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

                .players {
                    @include d-flex-align-center;
                    gap: 0.5rem;
                    margin-top: 2rem;

                    > .player {
                        flex-basis: calc(100% / 3 - (1rem / 3));
                        display: flex;
                        flex-direction: column;
                        border-radius: 10px;
                        gap: 0.5rem;
                        background-color: $deep-blue;
                        padding: 1.5rem;

                        .player-image {
                            border: 1px solid lime;
                            border-radius: 12px;
                            @include d-flex-align-center;
                            justify-content: center;
                            background-color: $dark-blue;
                            aspect-ratio: 6/5;
                            
                            background-repeat: no-repeat;
                            background-size: contain;
                            background-position: right;
                        }

                        .game-info {
                            @include d-flex-align-center;
                            justify-content: center;
                            // align-items: space-between;
                            padding: 1rem 0.5rem;
                            text-align: center;

                            .title-description {
                                @include d-flex-align-center;
                                justify-content: center;
                                flex-direction: column;
                                gap: 1rem;

                                h3 {
                                    font-size: 1.5rem;
                                }
    
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
    
                                .buttons {
                                    display: flex;
                                    justify-content: center;
                                    button {
                                        padding: 0.5rem;
                                        border: 0;
                                        border-radius: 50%;
                                        background-color: $full-green;
                                        margin-inline: 0.3rem;
                                        cursor: pointer;
                                        svg {
                                            width: 20px;
                                            aspect-ratio: 1;
                                            @include d-flex-align-center;
                                            justify-content: center;
                                            color: $dark-blue;
                                        }
                                    }
                                }
    
                                span {
                                    font-weight: bold;
                                    font-size: 2rem;
                                }

                                #view-more {
                                    height: 50px;
                                    width: 120px;
                                    border-radius: 7px;
                                }
                            }

                        }
                    }
                }
            }
        }
    }

    
</style>