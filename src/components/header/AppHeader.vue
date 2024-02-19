
<script>
    // Js componente
    export default {
        name: 'AppHeader',
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
        <div class="container">
            <!-- Logo -->
            <figure class="logo">
                <img src="../../assets/img/menulogo.png" alt="RaxG">
            </figure>
    
            <!-- Menu -->
            <nav>
                <ul>
                    <li v-for="(menu_voice, index) in menu" :key="index" >
                        <a href="#">
                            {{ menu_voice }}
                            <!-- <img v-if="menu_voice != 'tournament' && menu_voice != 'contact'" src="../../assets/img/image.svg" alt=""> -->
                            <svg v-if="menu_voice != 'tournament' && menu_voice != 'contact'" class="svg-inline--fa fa-angle-down" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="angle-down" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" data-fa-i2svg=""><path fill="currentColor" d="M192 384c-8.188 0-16.38-3.125-22.62-9.375l-160-160c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L192 306.8l137.4-137.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-160 160C208.4 380.9 200.2 384 192 384z"></path></svg>
                        </a>
                    </li>
                </ul>
            </nav>
    
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

        .container {
            @include d-flex-align-center;
            justify-content: space-between;
            color: white;

            nav {
                ul {
                    @include d-flex-align-center;
                    gap: 1rem;

                    li {
                        list-style-type: none;
                        a {
                            text-decoration: none;
                            color: white;
                            text-transform: uppercase;

                            @include d-flex-align-center;
                            gap: 0.2rem;

                            > svg {
                                height: 20px;
                            }

                            &:hover {
                                color: $full-green;
                            }
                        }
                    }
                }
            }

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


    }

    
</style>