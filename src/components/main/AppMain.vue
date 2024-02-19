

<script>
    // Js componente
    import Section1 from './Section1.vue';
    import Features from './Features.vue';
    import LiveStreaming from './LiveStreaming.vue';

    export default {
        name: 'AppMain',
        components: {
            Section1,
            Features,
            LiveStreaming
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
    <LiveStreaming />
</template>


<style lang="scss" scoped>
    /* stile del componente */

    
</style>