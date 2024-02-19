
<script>
    // Js componente
    export default {
        name: 'AppMain',
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
    <section id="experience" class="">
        <div class="container">
            <div class="col">

            </div>
            <div class="col">
                <span>12 year experience</span>
                <h2>we are the best gaming company</h2>
                <p>Nulla quis lorem ut libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, at tellus. Cras ultricies ligula sed magna ivamus magna justo, dictum porta.</p>
            </div>
        </div>
    </section>
    
</template>


<style lang="scss" scoped>
    /* stile del componente */

    @use '../../assets/styles/partials/variables' as *;
    @use '../../assets/styles/partials/mixins' as *;

    #experience {
        background-color: $dark-blue;
        height: 500px;

        .container {
            display: flex;
            justify-content: center;
            height: 100%;

            .col {
                flex-basis: 50%;
                border: 1px solid lime;
                height: 100%;
                padding: 1rem;
                color: white;
            }
        }
    }
    
</style>