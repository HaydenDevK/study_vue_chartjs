<script>
import { Line } from 'vue-chartjs'

export default {
  extends: Line,
  data () {
    return {
      chartData: {
        labels: ["11월 21일",	"11월 22일",	"11월 23일",	"11월 24일",	"11월 25일",	"11월 26일",	"11월 27일"],
        datasets: [
          {
            label: '코로나 확진자',
            data: [2827, 2698, 4115, 3937, 3899, 4067, 3928],
            fill: false,
            borderColor: 'blue',
            backgroundColor: '#F1F1F1',
            borderWidth: 1
          }
        ]
      },
      options: {
        scales: {
          yAxes: [{
            ticks: {
              beginAtZero: true // y축 0부터 보여주기
            },
            gridLines: {
              display: true
            }
          }],
          xAxes: [ {
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
