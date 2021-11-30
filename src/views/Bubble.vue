<template>
  <div>
    <h3>Bubble Chart Example in Vue</h3>
    <bubble-chart :chart-data="datacollection" :options="options"></bubble-chart>
    <button @click="onRequest()">Request</button>
  </div>
</template>

<script>
import BubbleChart from '@/components/BubbleChart'

export default {
  components: {
    BubbleChart
  },
  data () {
    return {
      datacollection: {
        datasets: []
      },
      options: {
        legend: {
          display: true
        },
        title: {
          display: true,
          text: 'Chart.js Bubble Chart'
        },
        responsive: true,
        maintainAspectRatio: false
      }
    }
  },
  mounted () {
    this.onRequest()
  },
  methods: {
    onReset() {
      // Q. this.datacollection.datasets 배열을 초기화하려고 했는데, 초기화가 안되어서, this.datacollection 자체를 초기화했는데, 왜 datasets 초기화가 안된건지

      // 첫번째 시도
      // this.datacollection.datasets = []

      // 두번째 시도
      // const emptyArr = []
      // this.datacollection.datasets = emptyArr

      // 세번째 시도
      // this.datacollection.datasets.splice(0, this.datacollection.datasets.length)

      // 네번째 시도
      // this.datacollection.datasets.length = 0

      this.datacollection = {
        datasets: []
      }
    },
    onRequest() {
      // 기존 데이터 초기화
      this.onReset()

      // 새로운 데이터 호출
      const response = [
        {
          id: '홍길동',
          x: 234.235,
          y: 596.563
        },
        {
          id: '홍길동',
          x: 234.235,
          y: 596.563
        },
        {
          id: '홍길동',
          x: 234.235,
          y: 596.563
        },
        {
          id: '홍길동',
          x: 234.235,
          y: 596.563
        },
        {
          id: '홍길동',
          x: 234.235,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 596.563,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 596.563,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 596.563,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 234.235,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 234.235,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 234.235,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 234.235,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 234.235,
          y: 596.563
        },
        {
          id: '김첨지',
          x: 234.235,
          y: 596.563
        },
        {
          id: 'a',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'a',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'a',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'a',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'b',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'c',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'd',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'e',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'f',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'g',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        },
        {
          id: 'h',
          x: this.getRandomInt(),
          y: this.getRandomInt()
        }
      ]

      // 가공해서 붙이기
      this.getDataSets(response)
    },
    getDataSets (response) {
      let newResponse = []
      for (let obj of response) {
        const indexId = newResponse.findIndex(ele => {
          return ele.label === obj.id
        })
        const indexAll = newResponse.findIndex(ele => {
          return ele.data[0].id === obj.id && ele.data[0].x === obj.x && ele.data[0].y === obj.y
        })

        if (indexAll > -1) {
          newResponse[indexAll].data[0].r += 10
        }
        else if (indexId > -1) {
          obj.r = 10
          newResponse[indexId].data.push(obj)
        }
        else {
          obj.r = 10
          newResponse.push({
            label: obj.id,
            data: [obj], // 배열로 감싸야함
            borderWidth: 1,
            backgroundColor: `rgba(${this.getRandomRgb()}, ${this.getRandomRgb()}, ${this.getRandomRgb()}, 0.5)`
          })
        }
      }
      this.datacollection.datasets = newResponse
    },
    getRandomInt () {
      return Math.floor(Math.random() * (100)) + 5
    },
    getRandomRgb () {
      return Math.floor(Math.random() * 256)
    }
  }
}
</script>
