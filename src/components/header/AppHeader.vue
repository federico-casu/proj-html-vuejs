
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
                </button>
            </div>
        </div>

        <div id="cta" class="container">
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
                }
            }
        }

        #cta {
            color: white;
            text-align: center;
            text-transform: uppercase;
            // height: 85%;
            
        
            @include d-flex-align-center;
            flex-direction: column;
            // justify-content: center;
            // height: 100%;
            
            margin-top: 100px;
            gap: 1.5rem;

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