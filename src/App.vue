<template>
  <goldenLayout id="app">
    <glCol>
      <Exchange />
    </glCol>
    <glCol>
      <Pairs />
    </glCol>
    <glCol>
      <Trades />
    </glCol>
  </goldenLayout>
</template>

<script>
  import goldenLayout from 'vue-golden-layout'
  import glCol from 'vue-golden-layout'
  import Exchange from './components/Exchange'
  import Pairs from './components/Pairs'
  import Trades from './components/Trades'
  export default {
    name: 'App',
    components: {
      Exchange,
      Pairs,
      Trades,
      goldenLayout,
      glCol
    }
  }

</script>

<style>
  @import 'golden-layout/src/css/goldenlayout-light-theme.css';

  html,
  body {
    margin: 0px;
    padding: 0px;
    height: 100%;
  }

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    text-align: center;
    display: grid;
    grid-template-columns: auto auto auto;
    min-height: 100%;
  }

</style>
