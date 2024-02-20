

<script>
    // Js componente
    export default {
        name: 'UpcomingMatch',
        data() {
            return {
                sections: [
                    {
                        name: 'All',
                        active: true
                    },
                    {
                        name: 'Pubg',
                        active: false
                    },
                    {
                        name: 'COD',
                        active: false
                    },
                    {
                        name: 'AC',
                        active: false
                    },
                    {
                        name: 'MCX',
                        active: false
                    }
                ],
                match: [
                    {
                        player1: {
                            name: 'Ninja Gaming',
                            image: '1.png'
                        },
                        player2: {
                            name: 'Witch Gaming',
                            image: '5.png'
                        },
                        game: 'PUBG Battleground',
                        time: '10.45',
                        active: true
                    },
                    {
                        player1: {
                            name: 'King Gaming',
                            image: '2.png'
                        },
                        player2: {
                            name: 'Witch Astro',
                            image: '6.png'
                        },
                        game: "Assassin's Creed",
                        time: '09.45',
                        active: false
                    },
                    {
                        player1: {
                            name: 'Dgn Gaming',
                            image: 't5.png'
                        },
                        player2: {
                            name: 'Joker Gaming',
                            image: 't6.png'
                        },
                        game: 'Mortal Combat X',
                        time: '08.45',
                        active: false
                    },
                    {
                        player1: {
                            name: 'Shark Gaming',
                            image: 't7.png'
                        },
                        player2: {
                            name: 'Krull Gaming',
                            image: 't8.png'
                        },
                        game: 'Call Of Duty',
                        time: '04.45',
                        active: false
                    }
                ],
                currentFilter: 'All'
            }
        },
        methods: {
            toggleActiveRow(element) {
                this.match.forEach(item => {
                    if (item.active === true) {
                        item.active = !item.active;
                    }
                });
                element.active = !element.active
            },
            toggleActiveFilter(element) {
                this.sections.forEach(item => {
                    if (item.active === true) {
                        item.active = !item.active;
                        this.currentFilter = element.name;
                    }
                });
                element.active = !element.active;
            },
            checkFilter(str1, str2) {
                switch (str1) {
                    case 'Pubg':
                        if (str2 === 'PUBG Battleground') {
                            return true
                        } else {
                            return false;
                        }
                    case 'COD':
                        if (str2 === 'Call Of Duty') {
                            return true
                        } else {
                            return false;
                        }
                    case 'AC':
                        if (str2 === "Assassin's Creed") {
                            return true
                        } else {
                            return false;
                        }
                    case 'MCX':
                        if (str2 === 'Mortal Combat X') {
                            return true
                        } else {
                            return false;
                        }
                    case 'All':
                        return true;
                    default:
                        return false;
                }
            }
        }
    }
</script>


<template>
    <!-- html componente -->
    <section id="trending-battle">
        <div class="container">
            <span class="sectionLittleTitle">Trending Battle</span>
            <h2 class="sectionTitle">Upcoming Match</h2>
            <ul>
                <li @click="toggleActiveFilter(section)" v-for="(section, index) in sections" :key="index" :class="currentFilter === section.name ? 'active-section': ''">{{ section.name }}</li>
            </ul>
            <div v-show="checkFilter(currentFilter, item.game)" v-for="(item, index) in match" :key="index" class="row" @click="toggleActiveRow(item)" :class="item.active ? 'row-active' : ''">
                <!-- primo giocatore -->
                <div class="player">
                    <figure class="player-image">
                        <img :src="`../../src/assets/img/${item.player1.image}`" :alt="item.player1.name">
                    </figure>
                    <div class="player-info">
                        <span class="sectionLittleTitle">Italy</span>
                        <h3>{{ item.player1.name }}</h3>
                    </div>
                </div>
                <!-- versus -->
                <div class="versus">
                    <span>VS</span>
                </div>
                <!-- secondo giocatore -->
                <div class="player">
                    <figure class="player-image">
                        <img :src="`../../src/assets/img/${item.player2.image}`" :alt="item.player2.name">
                    </figure>
                    <div class="player-info">
                        <span class="sectionLittleTitle">India</span>
                        <h3>{{ item.player2.name }}</h3>
                    </div>
                </div>
                <div class="game-info">
                    <h2 class="game-name">{{ item.game }}</h2>
                    <p class="game-description">
                        Nulla quis lorem ut libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna ivamus magna justo, dictum porta.
                    </p>
                </div>
                <div class="time-details" :class="item.active ? 'time-details-active' : ''">
                    <span>{{ item.time }}</span>
                    <p>1st November, 2022</p>
                    <div class="buttons">
                        <button id="youtube" :class="item.active ? 'button-active' : ''">
                            <svg :class="item.active ? 'svg-active' : ''" class="svg-inline--fa fa-youtube" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="youtube" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg=""><path fill="currentColor" d="M549.7 124.1c-6.281-23.65-24.79-42.28-48.28-48.6C458.8 64 288 64 288 64S117.2 64 74.63 75.49c-23.5 6.322-42 24.95-48.28 48.6-11.41 42.87-11.41 132.3-11.41 132.3s0 89.44 11.41 132.3c6.281 23.65 24.79 41.5 48.28 47.82C117.2 448 288 448 288 448s170.8 0 213.4-11.49c23.5-6.321 42-24.17 48.28-47.82 11.41-42.87 11.41-132.3 11.41-132.3s0-89.44-11.41-132.3zm-317.5 213.5V175.2l142.7 81.21-142.7 81.2z"></path></svg>
                        </button>
                        
                        <button id="chat" :class="item.active ? 'button-active' : ''">
                            <svg :class="item.active ? 'svg-active' : ''" class="svg-inline--fa fa-message" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="message" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M511.1 63.1v287.1c0 35.25-28.75 63.1-64 63.1h-144l-124.9 93.68c-7.875 5.75-19.12 .0497-19.12-9.7v-83.98h-96c-35.25 0-64-28.75-64-63.1V63.1c0-35.25 28.75-63.1 64-63.1h384C483.2 0 511.1 28.75 511.1 63.1z"></path></svg>
                        </button>
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

    #trending-battle {
        background-color: $dark-blue;
        color: white;
        text-align: center;

        .container {
            padding: 2rem 0;
            @include d-flex-align-center;
            flex-direction: column;
            gap: 1rem;
            ul {
                @include d-flex-align-center;
                justify-content: center;
                gap: 1rem;

                li:hover {
                    color: $full-green;
                    cursor: pointer;
                }

                .active-section {
                    color: $full-green;
                }
            }
            .row {
                @include d-flex-align-center;
                justify-content: space-between;
                // border: 1px solid red;
                border-radius: 10px;
                padding: 1.5rem;
                margin-top: 2rem;
                cursor: pointer;

                background-color: $deep-blue;

                
                .player {
                    // border: 1px solid lime;
                    border-radius: 10px;
                    max-width: 20%;

                    .player-image {
                        background-color: $dark-blue;
                        
                        width: 200px;
                        aspect-ratio: 1;
                        @include d-flex-align-center;
                        justify-content: center;
                        
                    }

                    .player-info {
                        text-align: start;
                        padding: 1rem ;
                        background-color: #152257;

                        h3 {
                            margin-top: 0.5rem;
                        }
                    }

                }

                .versus {
                    // border: 1px solid orange;
                    font-size: 2rem;
                    padding: 2rem;
                    color: $full-green;
                    background-color: $dark-blue;
                    border-radius: 10px;
                }

                .game-info {
                    max-width: 30%;
                    text-align: start;
                    // border: 1px solid yellow;
                    display: flex;
                    flex-direction: column;
                    gap: 0.5rem;
                }

                .time-details {
                    // border: 1px solid salmon;
                    aspect-ratio: 1;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    gap: 0.5rem;
                    padding: 1rem;
                    background-color: $dark-blue;
                    border-radius: 10px;

                    

                    > span {
                        font-weight: bold;
                        font-size: 2rem;
                    }

                    .buttons {
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

                            .svg-active {
                                color: white;
                            }
                        }

                        .button-active {
                            background-color: $dark-blue;
                        }
                    }
                }

                .time-details-active {
                    background-color: $light-green;
                    color: $dark-blue;
                }
            }

            .row-active {
                background-color: #343286;
            }
        }
    }



    // .row.active {
    //     background-color: $soft-deep-blue;

    //     .time-details {
    //         background-color: $light-green;
    //         color: $dark-blue;

    //         .buttons {
    //             button {
    //                 color: white;
    //                 background-color: $dark-blue;
    //             }
    //         }
    //     }
    // }
    
</style>