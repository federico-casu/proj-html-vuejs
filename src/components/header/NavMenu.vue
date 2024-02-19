

<script>
    // Js componente
    export default {
        name: 'NavMenu',
        props: {
            propsMenuVoices: Array
        },
        data() {
            return {
                
            }
        },
        methods: {
            
        }
    }
</script>


<template>
    <!-- html componente -->
    <nav>
        <ul>
            <li v-for="(menu_voice, index) in propsMenuVoices" :key="index" >
                <a href="#">
                    {{ menu_voice }}
                    <!-- <img v-if="menu_voice != 'tournament' && menu_voice != 'contact'" src="../../assets/img/image.svg" alt=""> -->
                    <svg v-if="menu_voice != 'tournament' && menu_voice != 'contact'" class="svg-inline--fa fa-angle-down" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="angle-down" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" data-fa-i2svg=""><path fill="currentColor" d="M192 384c-8.188 0-16.38-3.125-22.62-9.375l-160-160c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L192 306.8l137.4-137.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-160 160C208.4 380.9 200.2 384 192 384z"></path></svg>
                </a>
            </li>
        </ul>
    </nav>
    
</template>


<style lang="scss" scoped>
    /* stile del componente */

    @use '../../assets/styles/partials/variables' as *;
    @use '../../assets/styles/partials/mixins' as *;

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
</style>