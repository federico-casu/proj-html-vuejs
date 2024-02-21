

<script>
    // Js componente
    export default {
        name: 'Features',
        data() {
            return {
                features: [
                    {
                        image: 'feature1.png',
                        name: 'Live Streaming',
                        description: 'Nulla porttitor accumsan tincidunt. Pellentesque in.'
                    },
                    {
                        image: 'feature2.png',
                        name: 'Gaming News',
                        description: 'Nulla porttitor accumsan tincidunt. Pellentesque in.'
                    },
                    {
                        image: 'feature3.png',
                        name: 'Great Tournament',
                        description: 'Nulla porttitor accumsan tincidunt. Pellentesque in.'
                    },
                    {
                        image: 'feature4.png',
                        name: 'Award Ceremony',
                        description: 'Nulla porttitor accumsan tincidunt. Pellentesque in.'
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
    <section id="features">
        <div class="container">
            <div class="col feature-cards">
                <div v-for="(card, index) in features" :key="index" class="card">
                    <figure>
                        <img :src="`../../src/assets/img/${card.image}`" :alt="card.name">
                    </figure>
                    <h4>{{ card.name }}</h4>
                    <p>{{ card.description }}</p>
                </div>
            </div>
            <div class="col text">
                <span>our extrem feature</span>
                <h2>the best gaming arena on the world!</h2>
                <p>Nulla quis lorem ut libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna ivamus magna justo, dictum porta.</p>
            </div>
        </div>
    </section>

</template>


<style lang="scss" scoped>
    /* stile del componente */

    @use '../../assets/styles/partials/variables' as *;
    @use '../../assets/styles/partials/mixins' as *;

    #features {
        background-color: #1a1943;
        background-image: url('../../assets/img/Vector.png');
        @include bg-center-cover;
        padding: 3rem 0;

        .container {
            @include d-flex-align-center;
            // border: 1px solid purple;
            

            .col {
                flex-basis: 50%;
                padding: 3rem;
                color: white;
            }

            .feature-cards {
                order: 1;
                @include d-flex-align-center;
                flex-wrap: wrap;
                gap: 1rem;

                .card {
                    flex-basis: calc(100% / 2 - 0.5rem);
                    aspect-ratio: 1;
                    text-align: center;
                    @include d-flex-align-center;
                    gap: 0.5rem;
                    justify-content: center;
                    flex-direction: column;
                    // border: 1px solid red;
                    border-radius: 12px;
                    background-color: $soft-deep-blue;

                    &:hover {
                        background-color: $light-green;
                        color: $deep-blue;
                    }

                    figure {
                        width: 80px;
                        aspect-ratio: 1;
                        border-radius: 50%;
                        background-color: $deep-blue;
                        padding: 1rem;
                    }
                }
            }
    
            .text {
                display: flex;
                flex-direction: column;
                gap: 1rem;
                font-size: 14px;
        
                > span {
                    text-transform: uppercase;
                    color: $full-green;
                }
        
                h2 {
                    text-transform: capitalize;
                    font-size: 2.2rem;
                }
               
            }
        }
    }


    
</style>