

<script>
    // Js componente
    export default {
        name: 'LatestNews',
        data() {
            return {
                news: [
                    {
                        name: 'Ninja Warrior Gaming',
                        image: 'b1.png',
                    },
                    {
                        name: 'Gost Rider Returns',
                        image: 'b2.png',
                    },
                    {
                        name: 'Call Of Duty 4',
                        image: 'b3.png',
                    },
                    {
                        name: 'Mortal Combat X',
                        image: 'b4.png',
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
    <section id="latest-news">
        <div class="container">
            <div class="overview">
                <span class="sectionLittleTitle">Latest News</span>
                <div class="title-and-buttons">
                    <h2 class="sectionTitle">Stay Updated With our<br>Latest News Articles</h2>
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
                <div class="news">
                    <div v-for="(item, index) in news" :key="index" class="item">
                        <figure class="item-image">
                            <img :src="`../../src/assets/img/${item.image}`" :alt="item.name">
                        </figure>
                        <div class="item-info">
                            <div class="title-description">
                                <h3>{{ item.name }}</h3>
                                <div class="channel-date">
                                    <span class="channel">
                                        <svg class="svg-inline--fa fa-youtube" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="youtube" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg=""><path fill="currentColor" d="M549.7 124.1c-6.281-23.65-24.79-42.28-48.28-48.6C458.8 64 288 64 288 64S117.2 64 74.63 75.49c-23.5 6.322-42 24.95-48.28 48.6-11.41 42.87-11.41 132.3-11.41 132.3s0 89.44 11.41 132.3c6.281 23.65 24.79 41.5 48.28 47.82C117.2 448 288 448 288 448s170.8 0 213.4-11.49c23.5-6.321 42-24.17 48.28-47.82 11.41-42.87 11.41-132.3 11.41-132.3s0-89.44-11.41-132.3zm-317.5 213.5V175.2l142.7 81.21-142.7 81.2z"></path></svg>
                                        By Admin
                                    </span>
                                    <hr>
                                    <span class="date">
                                        <svg class="svg-inline--fa fa-calendar-days" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="calendar-days" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" data-fa-i2svg=""><path fill="currentColor" d="M160 32V64H288V32C288 14.33 302.3 0 320 0C337.7 0 352 14.33 352 32V64H400C426.5 64 448 85.49 448 112V160H0V112C0 85.49 21.49 64 48 64H96V32C96 14.33 110.3 0 128 0C145.7 0 160 14.33 160 32zM0 192H448V464C448 490.5 426.5 512 400 512H48C21.49 512 0 490.5 0 464V192zM64 304C64 312.8 71.16 320 80 320H112C120.8 320 128 312.8 128 304V272C128 263.2 120.8 256 112 256H80C71.16 256 64 263.2 64 272V304zM192 304C192 312.8 199.2 320 208 320H240C248.8 320 256 312.8 256 304V272C256 263.2 248.8 256 240 256H208C199.2 256 192 263.2 192 272V304zM336 256C327.2 256 320 263.2 320 272V304C320 312.8 327.2 320 336 320H368C376.8 320 384 312.8 384 304V272C384 263.2 376.8 256 368 256H336zM64 432C64 440.8 71.16 448 80 448H112C120.8 448 128 440.8 128 432V400C128 391.2 120.8 384 112 384H80C71.16 384 64 391.2 64 400V432zM208 384C199.2 384 192 391.2 192 400V432C192 440.8 199.2 448 208 448H240C248.8 448 256 440.8 256 432V400C256 391.2 248.8 384 240 384H208zM320 432C320 440.8 327.2 448 336 448H368C376.8 448 384 440.8 384 432V400C384 391.2 376.8 384 368 384H336C327.2 384 320 391.2 320 400V432z"></path></svg>
                                        Oct 25, 2022
                                    </span>
                                </div>
                                <button>
                                    <span>read more</span>
                                    <svg class="svg-inline--fa fa-right-long" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="right-long" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M504.3 273.6l-112.1 104c-6.992 6.484-17.18 8.218-25.94 4.406c-8.758-3.812-14.42-12.45-14.42-21.1L351.9 288H32C14.33 288 .0002 273.7 .0002 255.1S14.33 224 32 224h319.9l0-72c0-9.547 5.66-18.19 14.42-22c8.754-3.809 18.95-2.075 25.94 4.41l112.1 104C514.6 247.9 514.6 264.1 504.3 273.6z"></path></svg>
                                </button>
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

    #latest-news {
        background-color: $dark-blue;
        color: white;
        
        padding-block: 7rem 10rem;

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

                .news {
                    @include d-flex-align-center;
                    gap: 0.5rem;
                    margin-top: 2rem;

                    > .item {
                        flex-basis: calc(100% / 4 - (1.5rem / 4));
                        display: flex;
                        flex-direction: column;
                        gap: 0.5rem;
                        background-color: $deep-blue;
                        border-radius: 12px;
                        padding-bottom: 1rem;

                        &:hover {
                            .member-image {
                                #socials {
                                    @include d-flex-align-center;
                                }
                            }
                        }

                        .item-info {
                            @include d-flex-align-center;
                            justify-content: center;
                            flex-direction: column;
                            text-align: center;
                            
                            padding: 0.7rem 0;

                            .title-description {
                                @include d-flex-align-center;
                                justify-content: center;
                                flex-direction: column;
                                gap: 1.5rem;

                                padding: 0.5rem 0;

                                .channel-date {
                                    display: flex;
                                    gap: 0.5rem;

                                    hr {
                                        border: 1px solid $full-green;
                                    }

                                    svg {
                                        width: 20px;
                                        aspect-ratio: 1;
                                        color: $full-green;
                                    }

                                    .channel,
                                    .date {
                                        @include d-flex-align-center;
                                        gap: 0.5rem;
                                    }
                                }

                                button {
                                    color: $deep-blue;
                                    background-color: $light-green;
                                    border: 0;
                                    height: 50px;
                                    cursor: pointer;

                                    @include d-flex-align-center;
                                    border-radius: 5px;
                                    padding: 0.5rem 1rem;
                                    gap: 0.5rem;
                                    
                                    > span {
                                        text-transform: capitalize;
                                    }
                                    &:hover > svg {
                                        position: relative;
                                        left: 0.3rem;
                                    }

                                    > svg {
                                        height: 15px;
                                        
                                    }
                                }
                            }
                        }
                    }
                }
            }
        }
    }

    
</style>