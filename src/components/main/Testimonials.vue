

<script>
    // Js componente
    export default {
        name: 'Testimonials',
        data() {
            return {
                testimonials: [ 'test1.png', 'test2.png', 'test3.png', 'test4.png' ]
            }
        },
        methods: {
            
        }
    }
</script>


<template>
    <!-- html componente -->
    <section id="testimonials">
        <div class="container">
            <div class="overview">
                <div class="title">
                    <span class="sectionLittleTitle">Testimonials</span>
                    <h2 class="sectionTitle">What Our Client Say</h2>
                </div>
                <div class="clients">
                    <div v-for="(testimonial, index) in testimonials" :key="index" class="testimonial">
                        <figure class="testimonial-image">
                            <img :src="`../../src/assets/img/${testimonial}`" :alt="testimonial">
                        </figure>
                    </div>
                    <!-- buttons -->
                    
                    <button id="left">
                        <svg class="svg-inline--fa fa-arrow-left-long" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="arrow-left-long" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M9.375 233.4l128-128c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25L109.3 224H480c17.69 0 32 14.31 32 32s-14.31 32-32 32H109.3l73.38 73.38c12.5 12.5 12.5 32.75 0 45.25c-12.49 12.49-32.74 12.51-45.25 0l-128-128C-3.125 266.1-3.125 245.9 9.375 233.4z"></path></svg>
                    </button>
                    <button id="right">
                        <svg class="svg-inline--fa fa-arrow-right-long" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="arrow-right-long" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M502.6 278.6l-128 128c-12.51 12.51-32.76 12.49-45.25 0c-12.5-12.5-12.5-32.75 0-45.25L402.8 288H32C14.31 288 0 273.7 0 255.1S14.31 224 32 224h370.8l-73.38-73.38c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0l128 128C515.1 245.9 515.1 266.1 502.6 278.6z"></path></svg>
                    </button>
                </div>
            </div>
        </div>
    </section>
    
</template>


<style lang="scss" scoped>
    /* stile del componente */
    @use '../../assets/styles/partials/variables' as *;
    @use '../../assets/styles/partials/mixins' as *;

    #testimonials {
        background-color: $deep-blue;
        background-image: url('../../assets/img/test-group.png'), url('../../assets/img/test-grouptwo.png');
        background-repeat: no-repeat, no-repeat;
        background-size: 52%, 52%;
        background-position: right top, left bottom;
        color: white;
        padding: 7rem 0;

        .container {
            // border: 1px solid red;
    
            .overview {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                gap: 0.5rem;
    
                .title {
                    display: inline-block;
                    width: fit-content;
                    text-align: center;

                    .sectionTitle {
                        margin-top: 1rem;
                    }
    
                }
                
                .clients {
                    @include d-flex-align-center;
                    justify-content: center;
                    gap: 0.5rem;
                    margin-top: 2rem;
                    position: relative;
                    
                    button {
                        position: absolute;
                        top: 50%;
                        transform: translateY(-50%);

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

                    #left {
                        left: 10%;
                    }

                    #right {
                        right: 10%;
                    }

                    > .testimonial {
                        flex-basis: calc(100% / 4 - (1.5rem / 4));
                        width: calc(100% / 4 - (1.5rem / 4));
                        // height: 300px;
                        // height: 320px;
                        // display: flex;
                        // flex-direction: column;
                        // gap: 0.5rem;
                        background-color: #152257;

                        .testimonial-image {
                            position: relative;
                            width: 100%;
                            height: 100%;
                            
                            img {
                                height: 360px;
                                width: 100%;
                                object-fit: cover;
                            }

                            // #socials {
                            //     position: absolute;
                            //     bottom: 1rem;
                            //     left: 50%;
                            //     transform: translateX(-50%);
                                
                            //     color: white;

                            //     // @include d-flex-align-center;
                            //     display: none;
                            //     gap: 1rem;

                            //     li {
                            //         background-color: $soft-deep-blue;
                            //         width: 30px;
                            //         aspect-ratio: 1;
                            //         border-radius: 50%;
                            //         padding: 7px;

                            //         @include d-flex-align-center;
                            //         justify-content: center;

                            //         svg {
                            //             width: 20px;
                            //             aspect-ratio: 1;
                            //         }
                            //     }
                                
                            // }
                        }
                    }
                }
            }
        }
    }

    
</style>