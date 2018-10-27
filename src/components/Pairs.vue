<template>
  <div class="pairs-component">
    <h1>Pairs</h1>
    <select :value="pair.symbol" v-on:change="getPair">
      <option disabled value="">Please select a pair</option>
      <option v-for="pair in pairs" v-bind:value="pair.symbol" :key="pair.id"> {{ pair.symbol }}</option>
    </select>
  </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  name: 'Pairs',
  computed: {
    pairs () {
      return this.$store.state.pairs
    },
    pair () {
      return this.$store.state.pair
    }
  },
  methods: {
    ...mapActions(['receivePair', 'getTrades']),
    getPair (e) {
      let pair = e.target.value
      this.receivePair(pair)
      this.getTrades()
    }
  }
}
</script>
<style scoped>
.pairs-component {
  background-color: #4062bb;
}
h1 {
  margin-top: 100px;
  font-size: 40px;
  color: #e8edf4;
}
select {
  font-size: 18px;
  padding: 5px;
  color: #e8edf4;
  background-color: #52489c;
}
</style>
