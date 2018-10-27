<template>
  <golden-layout id="app">
    <gl-col>
      <Exchange />
    </gl-col>
    <gl-col>
      <Pairs />
    </gl-col>
    <gl-col>
      <Trades />
    </gl-col>
  </golden-layout>
</template>

<script>
  import vgl from 'vue-golden-layout/'
  import Exchange from './components/Exchange'
  import Pairs from './components/Pairs'
  import Trades from './components/Trades'
  export default {
    name: 'App',
    components: {
      Exchange,
      Pairs,
      Trades,
      vgl
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
