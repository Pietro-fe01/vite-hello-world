<script>
  import AppTitle from './components/AppTitle.vue';
  import Jumbotron from './components/JumbotronComponent.vue';

  export default {
    components: {
      AppTitle,
      Jumbotron
    }
  }
</script>

<template>
  <header>
    <AppTitle/>
  </header>

  <main>
    <Jumbotron/>
  </main>
</template>

<style scoped>
  header {
    text-align: center;
  }
</style>
