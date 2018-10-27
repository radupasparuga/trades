<template>
  <div class="trades-component">
    <h1>Trades</h1>
    <table>
      <tr>
        <th>Size</th>
        <th>Price</th>
        <th>Time</th>
      </tr>
      <tr v-for="trade in trades" :key="trade.id">
        <td class="amount">{{ trade.amount }}</td>
        <td class="price">{{ trade.price }}</td>
        <td class="datetime">{{ trade.datetime.slice(12, 19) }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Trades',
  computed: {
    trades () {
      return this.$store.state.trades
    }
  }
}
</script>
<style scoped>
.trades-component {
  background-color: #59c3c3;
}
h1 {
  font-size: 40px;
  margin-top: 100px;
  color: #e8edf4;
}
table {
  margin-left: auto;
  margin-right: auto;
  width: 100%;
  padding: 10px;
}
.amount {
  color: #e8edf4;
  font-size: 18px;
}
.price {
  color: white;
  font-size: 18px;
}
.datetime {
  color: #e8edf4;
  font-size: 18px;
}
</style>
