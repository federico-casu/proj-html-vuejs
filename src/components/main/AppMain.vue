

<script>
    // Js componente
    import Section1 from './Section1.vue';
    import Features from './Features.vue';
    import LiveStreaming from './LiveStreaming.vue';
    import UpcomingMatch from './UpcomingMatch.vue';
    import TrendingGames from './TrendingGames.vue';
    import KeepEyesOn from './KeepEyesOn.vue';
    import TeamMembers from './TeamMembers.vue';

    export default {
        name: 'AppMain',
        components: {
            Section1,
            Features,
            LiveStreaming,
            UpcomingMatch,
            TrendingGames,
            KeepEyesOn,
            TeamMembers
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
    <UpcomingMatch />
    <TrendingGames />
    <KeepEyesOn />
    <TeamMembers />
</template>


<style lang="scss" scoped>
    /* stile del componente */

    
</style>