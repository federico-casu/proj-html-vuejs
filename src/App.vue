
<script>

import AppHeader from './components/header/AppHeader.vue';
import AppMain from './components/main/AppMain.vue';
import AppFooter from './components/footer/AppFooter.vue';
import { store } from './store';

  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter
    },
    data() {
      return {
        store,
        menu: [ "home", "pages", "tournament", "shop", "blog", "contact" ] 
      }
    },
    methods: {

    }
  }

</script>

<template>

  <AppHeader />
  <AppMain />
  <AppFooter :propsMenu="menu" />

</template>

<style lang="scss">

  @use './assets/styles/general.scss' as *;
  @use './assets/styles/partials/mixins.scss' as *;
  @use './assets/styles/partials/variables.scss' as *;



</style>
