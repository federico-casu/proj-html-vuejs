

<script>
    // Js componente
    import Section1 from './Section1.vue';
    import Features from './Features.vue';

    export default {
        name: 'AppMain',
        components: {
            Section1,
            Features
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
    <Section1 />
    <Features />
</template>


<style lang="scss" scoped>
    /* stile del componente */

    
</style>