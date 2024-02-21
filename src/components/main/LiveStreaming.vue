

<script>
    // Js componente
    export default {
        name: 'LiveStreaming',
        data() {
            return {
                streamings: [
                    {
                        image: 'v-small1.png',
                        name: 'Call of Duty',
                        description: 'Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui.',
                        active: true
                    },
                    {
                        image: 'v-small2.png',
                        name: "Assassin's Creed",
                        description: 'Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui.',
                        active: false
                    }
                ]
            }
        },
        methods: {
            changeStream() {
                
            }
        }
    }
</script>


<template>
    <!-- html componente -->
    <section id="streaming">
        <div class="container">
            <div class="col active-stream">
                <figure>
                    <img src="../../assets/img/v-small1.png" alt="">
                    <div>
                        <button class="play-button">
                            <svg class="svg-inline--fa fa-play" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="play" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" data-fa-i2svg=""><path fill="currentColor" d="M361 215C375.3 223.8 384 239.3 384 256C384 272.7 375.3 288.2 361 296.1L73.03 472.1C58.21 482 39.66 482.4 24.52 473.9C9.377 465.4 0 449.4 0 432V80C0 62.64 9.377 46.63 24.52 38.13C39.66 29.64 58.21 29.99 73.03 39.04L361 215z"></path></svg>
                        </button>
                        <h4>Call of Duty</h4>
                    </div>
                </figure>
            </div>
            <div class="col overview">
                <span>live streaming</span>
                <div class="title-and-buttons">
                    <h2>checkout our live streaming</h2>
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
                <div class="streams">
                    <div v-for="(stream, index) in streamings" :key="index" class="col">
                        <figure>
                            <img :src="`../../src/assets/img/${stream.image}`" :alt="stream.name">
                        </figure>
                        <h4>{{ stream.name }}</h4>
                        <p>{{ stream.description }}</p>
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

    #streaming {
        padding: 5rem 0;
        background-image: url('../../assets/img/v-bg.png');
        background-color: rgba(32, 32, 70, 0.6);
        background-blend-mode: overlay;
        @include bg-center-cover;

        .container {
            display: flex;
            // border: 1px solid lime;
            gap: 1rem;

            .col {
                flex-basis: 50%;
                // padding: 3rem;
                color: white;
                // border: 2px solid black;
            }

            .active-stream {
                figure {
                    position: relative;
                    img {
                        width: 100%;
                    }

                    > div {
                        display: flex;
                        flex-direction: column;
                        align-items: center;
                        justify-content: center;
                        background-color: rgba($color: #121212, $alpha: 0.5);
                        border-radius: 30px;
                        width: 100%;
                        height: 100%;
                        gap: 0.5rem;
                        position: absolute;
                        top: 0;
                        // top: 50%;
                        // left: 50%;
                        // transform: translate(-50%, -50%);
                        button {
                            display: flex;
                            align-items: center;
                            justify-content: center;
                            border: 0;
                            border-radius: 50%;
                            background-color: $full-green;
                            width: 50px;
                            aspect-ratio: 1;
                            cursor: pointer;
                            svg {
                                width: 30px;
                                aspect-ratio: 1;
                                padding: 0.5rem;
                                color: white;
                            }
                        }
                    }
                }
            }

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

                > span {
                    font-weight: bold;
                    text-transform: capitalize;
                    color: $full-green;
                }

                h2 {
                    text-transform: capitalize;
                    font-size: 2.2rem;
                }

                .streams {
                    @include d-flex-align-center;
                    gap: 0.5rem;

                    > .col {
                        display: flex;
                        flex-direction: column;
                        gap: 0.5rem;
                    }
                }
            }
        }
    }
    
</style>