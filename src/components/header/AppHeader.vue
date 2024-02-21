
<script>
    // Js componente

    import NavMenu from './NavMenu.vue';

    export default {
        name: 'AppHeader',
        components: {
            NavMenu
        },
        data() {
            return {
               menu: [ "home", "pages", "tournament", "shop", "blog", "contact" ] 
            }
        },
        methods: {
            
        }
    }
</script>


<template>
    <!-- html componente -->

    <header>
        <div id="top-bar" class="container">
            <!-- Logo -->
            <figure class="logo">
                <img src="../../assets/img/menulogo.png" alt="RaxG">
            </figure>
    
            <!-- Menu -->
            <NavMenu :propsMenuVoices="menu"/>
    
            <div class="buttons">
                <button id="search">
                    <svg class="svg-inline--fa fa-magnifying-glass" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="magnifying-glass" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M500.3 443.7l-119.7-119.7c27.22-40.41 40.65-90.9 33.46-144.7C401.8 87.79 326.8 13.32 235.2 1.723C99.01-15.51-15.51 99.01 1.724 235.2c11.6 91.64 86.08 166.7 177.6 178.9c53.8 7.189 104.3-6.236 144.7-33.46l119.7 119.7c15.62 15.62 40.95 15.62 56.57 0C515.9 484.7 515.9 459.3 500.3 443.7zM79.1 208c0-70.58 57.42-128 128-128s128 57.42 128 128c0 70.58-57.42 128-128 128S79.1 278.6 79.1 208z"></path></svg>
                </button>
                
                <button id="cart">
                    <svg class="svg-inline--fa fa-bag-shopping" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="bag-shopping" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" data-fa-i2svg=""><path fill="currentColor" d="M112 112C112 50.14 162.1 0 224 0C285.9 0 336 50.14 336 112V160H400C426.5 160 448 181.5 448 208V416C448 469 405 512 352 512H96C42.98 512 0 469 0 416V208C0 181.5 21.49 160 48 160H112V112zM160 160H288V112C288 76.65 259.3 48 224 48C188.7 48 160 76.65 160 112V160zM136 256C149.3 256 160 245.3 160 232C160 218.7 149.3 208 136 208C122.7 208 112 218.7 112 232C112 245.3 122.7 256 136 256zM312 208C298.7 208 288 218.7 288 232C288 245.3 298.7 256 312 256C325.3 256 336 245.3 336 232C336 218.7 325.3 208 312 208z"></path></svg>
                    <span>0</span>
                    <div class="cart-items">
                        <ul>
                            <li>
                                <figure>
                                    <img src="../../assets/img/cart1.png" alt="">
                                </figure>
                                <div class="product-info">
                                    <h3>Sony PS5 White</h3>
                                    <span>Quality: $254</span>
                                </div>
                                <svg class="svg-inline--fa fa-xmark" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="xmark" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512" data-fa-i2svg=""><path fill="currentColor" d="M310.6 361.4c12.5 12.5 12.5 32.75 0 45.25C304.4 412.9 296.2 416 288 416s-16.38-3.125-22.62-9.375L160 301.3L54.63 406.6C48.38 412.9 40.19 416 32 416S15.63 412.9 9.375 406.6c-12.5-12.5-12.5-32.75 0-45.25l105.4-105.4L9.375 150.6c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L160 210.8l105.4-105.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-105.4 105.4L310.6 361.4z"></path></svg>
                            </li>
                            <li>
                                <figure>
                                    <img src="../../assets/img/cart2.png" alt="">
                                </figure>
                                <div class="product-info">
                                    <h3>A4 Tec Mouse</h3>
                                    <span>Quality: $121</span>
                                </div>
                                <svg class="svg-inline--fa fa-xmark" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="xmark" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512" data-fa-i2svg=""><path fill="currentColor" d="M310.6 361.4c12.5 12.5 12.5 32.75 0 45.25C304.4 412.9 296.2 416 288 416s-16.38-3.125-22.62-9.375L160 301.3L54.63 406.6C48.38 412.9 40.19 416 32 416S15.63 412.9 9.375 406.6c-12.5-12.5-12.5-32.75 0-45.25l105.4-105.4L9.375 150.6c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L160 210.8l105.4-105.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-105.4 105.4L310.6 361.4z"></path></svg>
                            </li>
                            <li>
                                <figure>
                                    <img src="../../assets/img/cart3.png" alt="">
                                </figure>
                                <div class="product-info">
                                    <h3>Gear VR Led</h3>
                                    <span>Quality: $514</span>
                                </div>
                                <svg class="svg-inline--fa fa-xmark" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="xmark" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512" data-fa-i2svg=""><path fill="currentColor" d="M310.6 361.4c12.5 12.5 12.5 32.75 0 45.25C304.4 412.9 296.2 416 288 416s-16.38-3.125-22.62-9.375L160 301.3L54.63 406.6C48.38 412.9 40.19 416 32 416S15.63 412.9 9.375 406.6c-12.5-12.5-12.5-32.75 0-45.25l105.4-105.4L9.375 150.6c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L160 210.8l105.4-105.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-105.4 105.4L310.6 361.4z"></path></svg>
                            </li>
                        </ul>

                        <div class="total-order">
                            <span>Total Order</span>
                            <span>$854.00</span>
                        </div>
                        <button class="check-out">CHECK OUT</button>
                    </div>
                </button>
            </div>
        </div>

        <div id="cta" class="container">
            <ul id="socials">
                <li>
                    <svg class="svg-inline--fa fa-facebook" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="facebook" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M504 256C504 119 393 8 256 8S8 119 8 256c0 123.8 90.69 226.4 209.3 245V327.7h-63V256h63v-54.64c0-62.15 37-96.48 93.67-96.48 27.14 0 55.52 4.84 55.52 4.84v61h-31.28c-30.8 0-40.41 19.12-40.41 38.73V256h68.78l-11 71.69h-57.78V501C413.3 482.4 504 379.8 504 256z"></path></svg>
                </li>
                <li>
                    <svg class="svg-inline--fa fa-twitter" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="twitter" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M459.4 151.7c.325 4.548 .325 9.097 .325 13.65 0 138.7-105.6 298.6-298.6 298.6-59.45 0-114.7-17.22-161.1-47.11 8.447 .974 16.57 1.299 25.34 1.299 49.06 0 94.21-16.57 130.3-44.83-46.13-.975-84.79-31.19-98.11-72.77 6.498 .974 12.99 1.624 19.82 1.624 9.421 0 18.84-1.3 27.61-3.573-48.08-9.747-84.14-51.98-84.14-102.1v-1.299c13.97 7.797 30.21 12.67 47.43 13.32-28.26-18.84-46.78-51.01-46.78-87.39 0-19.49 5.197-37.36 14.29-52.95 51.65 63.67 129.3 105.3 216.4 109.8-1.624-7.797-2.599-15.92-2.599-24.04 0-57.83 46.78-104.9 104.9-104.9 30.21 0 57.5 12.67 76.67 33.14 23.72-4.548 46.46-13.32 66.6-25.34-7.798 24.37-24.37 44.83-46.13 57.83 21.12-2.273 41.58-8.122 60.43-16.24-14.29 20.79-32.16 39.31-52.63 54.25z"></path></svg>
                </li>
                <li>
                    <svg class="svg-inline--fa fa-linkedin" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="linkedin" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" data-fa-i2svg=""><path fill="currentColor" d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"></path></svg>
                </li>
                <li>
                    <svg class="svg-inline--fa fa-instagram" aria-hidden="true" focusable="false" data-prefix="fab" data-icon="instagram" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" data-fa-i2svg=""><path fill="currentColor" d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"></path></svg> 
                </li>
            </ul>
            <span>welcome to raxg</span>
            <h1>are you ready for your<br>next challenge?</h1>
            <div class="buttons">
                <button>
                    <span>read more</span>
                    <svg class="svg-inline--fa fa-right-long" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="right-long" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M504.3 273.6l-112.1 104c-6.992 6.484-17.18 8.218-25.94 4.406c-8.758-3.812-14.42-12.45-14.42-21.1L351.9 288H32C14.33 288 .0002 273.7 .0002 255.1S14.33 224 32 224h319.9l0-72c0-9.547 5.66-18.19 14.42-22c8.754-3.809 18.95-2.075 25.94 4.41l112.1 104C514.6 247.9 514.6 264.1 504.3 273.6z"></path></svg>
                </button>
                <button>
                    <svg class="svg-inline--fa fa-play" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="play" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" data-fa-i2svg=""><path fill="currentColor" d="M361 215C375.3 223.8 384 239.3 384 256C384 272.7 375.3 288.2 361 296.1L73.03 472.1C58.21 482 39.66 482.4 24.52 473.9C9.377 465.4 0 449.4 0 432V80C0 62.64 9.377 46.63 24.52 38.13C39.66 29.64 58.21 29.99 73.03 39.04L361 215z"></path></svg>
                </button>
            </div>
        </div>

    </header>
    
</template>


<style lang="scss" scoped>
    /* stile del componente */

    @use '../../assets/styles/partials/mixins' as *;
    @use '../../assets/styles/partials/variables' as *;

    header {
        background-image: url('../../assets/img/banner1.png');
        @include bg-center-cover;
        height: 700px;
        padding: 1rem 0;

        #top-bar {
            @include d-flex-align-center;
            justify-content: space-between;
            color: white;
            // height: 15%;

            

            .buttons {
                @include d-flex-align-center;
                gap: 1rem;

                > button {
                    @include d-flex-align-center;
                    justify-content: center;
                    background-color: white;
                    height: 40px;
                    aspect-ratio: 1;
                    // padding: 10px;
                    border-radius: 50%;
                    color: $soft-deep-blue;
                    border: 0;
                    cursor: pointer;

                    > svg {
                        height: 20px;
                        aspect-ratio: 1;  
                    }
                }

                #cart {
                    position: relative;
                    &:hover {
                        .cart-items{
                            display: flex;
                        }
                    }

                    > span {
                        text-align: center;
                        position: absolute;
                        top: -0.5rem;
                        right: -0.3rem;
                        color: white;
                        background-color: $light-blue;
                        padding: 0.2rem 0.4rem;
                        border-radius: 50%;
                    }

                    .cart-items {
                        display: none;
                        position: absolute;
                        top: 100%;
                        right: 20%;
                        width: 300px;
                        color: white;

                        // display: flex;
                        flex-direction: column;
                        gap: 1rem;

                        z-index: 1;

                        background-color: rgba(32, 32, 70, 0.8);

                        padding: 1rem;

                        ul {
                            display: flex;
                            flex-direction: column;
                            gap: 0.5rem;
                            li {
                                @include d-flex-align-center;
                                color: white;
                                justify-content: space-between;

                                figure {
                                    border: 1px solid $full-green;
                                }

                                .product-info {
                                    display: flex;
                                    flex-direction: column;
                                    align-items: flex-start;
                                    gap: 0.5rem;
                                }

                                svg {
                                    width: 15px;
                                    color: $full-green;
                                }
                            }
                        }

                        .total-order {
                            @include d-flex-align-center;
                            justify-content: space-between;
                            font-size: 1rem;
                        }

                        .check-out {
                            background-color: $light-green;
                            border: 0;
                            color: $dark-blue;
                            font-size: 1rem;
                            font-weight: bold;

                            padding: 1rem 0;
                        }


                    }
                }
            }
        }

        #cta {
            color: white;
            text-align: center;
            text-transform: uppercase;
        
            @include d-flex-align-center;
            flex-direction: column;
            
            margin-top: 100px;
            gap: 1.5rem;

            position: relative;

            #socials {
                position: absolute;
                left: -7%;
                top: 50%;
                transform: translateY(-50%);
                                
                color: white;

                display: flex;
                flex-direction: column;
                gap: 1rem;

                li {
                    background-color: $soft-deep-blue;
                    width: 30px;
                    aspect-ratio: 1;
                    border-radius: 50%;
                    padding: 7px;

                    @include d-flex-align-center;
                    justify-content: center;

                    &:hover {
                        background-color: $full-green;
                    }

                    svg {
                        width: 20px;
                        aspect-ratio: 1;
                    }
                }
                                
            }

            > span {
                color: $full-green;
            }

            h1 {
                font-size: 3.2rem;
            }

            .buttons {
                @include d-flex-align-center;
                gap: 1.5rem;

                > button {
                    color: $deep-blue;
                    background-color: $light-green;
                    border: 0;
                    height: 50px;
                    cursor: pointer;
                }

                button:first-child {
                    @include d-flex-align-center;
                    border-radius: 5px;
                    padding: 0.5rem 1rem;
                    gap: 0.5rem;
                    
                    > span {
                        text-transform: capitalize;
                        // width: fit-content;
                    }
                    &:hover > svg {
                        position: relative;
                        left: 0.3rem;
                    }

                    > svg {
                        height: 15px;
                        
                    }
                }

                button:last-child { 
                    aspect-ratio: 1;
                    @include d-flex-align-center;
                    justify-content: center;
                    border-radius: 50%;
                    padding: 1rem;

                    > svg {
                        height: 100%;
                        text-align: center;
                    }
                }
            }

        }


    }

    
</style>