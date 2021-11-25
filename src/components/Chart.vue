<!-- Bar -->
<!--<script>-->
<!--import { Bar } from 'vue-chartjs'-->

<!--export default {-->
<!--  extends: Bar,-->
<!--  data () {-->
<!--    return {-->
<!--      chartdata: {-->
<!--        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],-->
<!--        datasets: [{-->
<!--          label: 'Number of Votes',-->
<!--          data: [12, 19, 3, 5, 2, 3],-->
<!--          backgroundColor: [-->
<!--            'rgba(255, 99, 132, 0.2)',-->
<!--            'rgba(54, 162, 235, 0.2)',-->
<!--            'rgba(255, 206, 86, 0.2)',-->
<!--            'rgba(75, 192, 192, 0.2)',-->
<!--            'rgba(153, 102, 255, 0.2)',-->
<!--            'rgba(255, 159, 64, 0.2)'-->
<!--          ],-->
<!--          borderColor: [-->
<!--            'rgba(255, 99, 132, 1)',-->
<!--            'rgba(54, 162, 235, 1)',-->
<!--            'rgba(255, 206, 86, 1)',-->
<!--            'rgba(75, 192, 192, 1)',-->
<!--            'rgba(153, 102, 255, 1)',-->
<!--            'rgba(255, 159, 64, 1)'-->
<!--          ],-->
<!--          borderWidth: 1-->
<!--        }]-->
<!--      },-->
<!--      options: {-->
<!--        responsive: true,-->
<!--        maintainAspectRatio: false,-->
<!--        animation: { duration: 5000 }-->
<!--      }-->
<!--    }-->
<!--  },-->
<!--  mounted () {-->
<!--    this.renderChart(this.chartdata, this.options)-->
<!--  }-->
<!--}-->
<!--</script>-->


<!-- Line -->
<!--<script>-->
<!--import { Line } from 'vue-chartjs'-->

<!--export default {-->
<!--  extends: Line,-->
<!--  data() {-->
<!--    return {-->
<!--      chartData: {-->
<!--        labels: ['January', 'February'],-->
<!--        datasets: [-->
<!--          {-->
<!--            label: 'Data One',-->
<!--            backgroundColor: '#9575CD',-->
<!--            data: [40, 20]-->
<!--          },{-->
<!--            label: 'Data Two',-->
<!--            backgroundColor: '#64B5F6',-->
<!--            data: [30, 40]-->
<!--          }-->
<!--        ],-->
<!--      },-->
<!--    };-->
<!--  },-->
<!--  mounted () {-->
<!--    this.renderChart(this.chartData, this.options)-->
<!--  }-->
<!--}-->
<!--</script>-->


<!-- Doughnut -->
<script>
import { Doughnut } from 'vue-chartjs'

export default {
  extends: Doughnut,
  data () {
    return {
      chartData: {
        labels: [
          'Red',
          'Blue',
          'Yellow',
          'green'
        ],
        datasets: [{
          label: 'My First Dataset',
          data: [300, 50, 100],
          backgroundColor: [
            'red',
            'blue',
            'yellow',
            'green'
          ],
          hoverOffset: 4
        }]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        layout: { padding: { top: 50, bottom: 50 } },
        elements: { arc: { borderWidth: 2 } },
        animation: { duration: 5000 }
      }
    }
  },
  mounted () {
    this.renderChart(this.chartData, this.options)
  }
}
</script>



<!-- 반응형? -->
<!-- Doughnut -->
<!--<script>-->
<!--import { Doughnut, mixins } from 'vue-chartjs'-->
<!--const { reactiveProp } = mixins-->

<!--export default {-->
<!--  extends: Doughnut,-->
<!--  mixins: [reactiveProp],-->
<!--  data () {-->
<!--    return {-->
<!--      chartData: null,-->
<!--      options: {-->
<!--        plugins: {-->
<!--          legend: {-->
<!--            // display: true,-->
<!--            // position: 'left',-->
<!--            labels: { boxWidth: 8, padding: 10, usePointStyle: true, pointStyle: 'circle', font: { size: 90 } },-->
<!--            fullSize: true,-->
<!--            align: 'center'-->
<!--          },-->
<!--          tooltip: {-->
<!--            boxWidth: 15,-->
<!--            bodyFont: { size: 80 }-->
<!--          }-->
<!--        },-->
<!--        responsive: true,-->
<!--        maintainAspectRatio: false,-->
<!--        layout: { padding: { top: 50, bottom: 50 } },-->
<!--        elements: { arc: { borderWidth: 2 } },-->
<!--        animation: { duration: 5000 }-->
<!--      }-->
<!--    }-->
<!--  },-->
<!--  mounted () {-->
<!--    this.fillData()-->
<!--    this.renderChart(this.chartData, this.options)-->
<!--  },-->
<!--  methods: {-->
<!--    fillData () {-->
<!--      this.chartData = {-->
<!--        labels: [this.getRandomInt(), this.getRandomInt()],-->
<!--        datasets: [-->
<!--          {-->
<!--            label: 'Data One',-->
<!--            backgroundColor: '#f87979',-->
<!--            data: [this.getRandomInt(), this.getRandomInt()]-->
<!--          }, {-->
<!--            label: 'Data One',-->
<!--            backgroundColor: '#f87979',-->
<!--            data: [this.getRandomInt(), this.getRandomInt()]-->
<!--          }-->
<!--        ]-->
<!--      }-->
<!--    },-->
<!--    getRandomInt () {-->
<!--      return Math.floor(Math.random() * (50 - 5 + 1)) + 5-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->
