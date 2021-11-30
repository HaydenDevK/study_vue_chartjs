<script>
import { Bar } from 'vue-chartjs'

export default {
  extends: Bar,
  data () {
    return {
      chartData: {
        labels: ['11월 21일', '11월 22일', '11월 23일', '11월 24일', '11월 25일', '11월 26일', '11월 27일'],
        datasets: [
          {
            label: '코로나 확진자',
            borderWidth: 1,
            borderColor: 'blue',
            // backgroundColor: 'mint',
            // pointBorderColor: 'red',
            data: [2827, 2698, 4115, 3937, 3899, 4067, 3928],
          }]
      },
      options: {
        scales: {
          yAxes: [{
            ticks: {
              beginAtZero: true
            },
            gridLines: {
              display: true
            }
          }],
          xAxes: [{
            gridLines: {
              display: false
            }
          }]
        },
        legend: {
          display: true
        },
        title: {
          display: true,
          text: '국내 코로나 확진자 현황 (11/21 ~ 11/27)'
        },
        responsive: true,
        maintainAspectRatio: false
      }
    }
  },
  mounted () {
    this.renderChart(this.chartData, this.options)
  }
}
</script>
