
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
                    <li v-for="(menu_voice, index) in menu" :key="index" ><a href="#">{{ menu_voice }}</a></li>
                </ul>
            </nav>
    
            <div class="buttons">
                <figure>
                    <img src="../../assets/img/image(1).svg" alt="magnifying glass">
                </figure>
                <figure>
                    <img src="../../assets/img/image(3).svg" alt="cart">
                </figure>
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

                > figure {
                    background-color: white;
                    height: 40px;
                    aspect-ratio: 1;
                    padding: 10px;
                    border-radius: 50%;

                    > img {
                        height: 20px;
                        aspect-ratio: 1;
                        
                    }
                }
            }
        }


    }

    
</style>