<script>
import { Doughnut } from 'vue-chartjs'

export default {
  extends: Doughnut,
  data () {
    return {
      chartData: {
        labels: ["화이자", "모더나", "얀센"],
        datasets: [{
          borderWidth: 1,
          borderColor: [
            'rgba(255, 99, 132, 1)',
            'rgba(54, 162, 235, 1)',
            'rgba(255, 206, 86, 1)'
          ],
          backgroundColor: [
            'rgba(255, 99, 132, 0.2)',
            'rgba(54, 162, 235, 0.2)',
            'rgba(255, 206, 86, 0.2)'
          ],
          data: [2117442,	714574, 13381]
        }]
      },
      options: {
        legend: {
          display: true
        },
        title: {
          display: true,
          text: '코로나 백신 추가접종자 백신 종류별 비율'
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
