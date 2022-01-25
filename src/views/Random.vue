<template>
  <div>
    <h3>Random Chart Example in Vue</h3>
    <random-chart :chart-data="datacollection"></random-chart>
    <button @click="fillData()">Randomize</button>
  </div>
</template>

<script>
import RandomChart from '@/components/RandomChart'

// chartData.datasets
export default {
  components: {
    RandomChart
  },
  data () {
    return {
      // datacollection: null // 에러남
      datacollection: {}
    }
  },
  mounted () {
    this.fillData()
  },
  methods: {
    fillData () {
      this.datacollection = {
        labels: [this.getRandomInt(), this.getRandomInt(), this.getRandomInt()],
        datasets: [
          {
            label: 'Data 1',
            backgroundColor: '#f87979',
            data: [this.getRandomInt(), this.getRandomInt(), this.getRandomInt()]
          },
          {
            label: 'Data 2',
            backgroundColor: '#dddd99',
            data: [this.getRandomInt(), this.getRandomInt(), this.getRandomInt()]
          },
        ]
      }
    },
    getRandomInt () {
      return Math.floor(Math.random() * (50 - 5 + 1)) + 5
    }
  }
}
</script>

<style>
.small {
  max-width: 600px;
  margin: 150px auto;
}
</style>
