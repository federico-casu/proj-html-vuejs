
<script>

import AppHeader from './components/header/AppHeader.vue';
import AppMain from './components/main/AppMain.vue';
import AppFooter from './components/footer/AppFooter.vue';

  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter
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

  <AppHeader />
  <AppMain />
  <AppFooter />

</template>

<style lang="scss">

  @use './assets/styles/general.scss' as *;
  @use './assets/styles/partials/mixins.scss' as *;
  @use './assets/styles/partials/variables.scss' as *;



</style>
