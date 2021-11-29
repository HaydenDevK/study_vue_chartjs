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
<!--<script>-->
<!--import { Doughnut } from 'vue-chartjs'-->

<!--export default {-->
<!--  extends: Doughnut,-->
<!--  data () {-->
<!--    return {-->
<!--      chartData: {-->
<!--        labels: [-->
<!--          'Red',-->
<!--          'Blue',-->
<!--          'Yellow',-->
<!--          'green'-->
<!--        ],-->
<!--        datasets: [{-->
<!--          label: 'My First Dataset',-->
<!--          data: [300, 50, 100],-->
<!--          backgroundColor: [-->
<!--            'red',-->
<!--            'blue',-->
<!--            'yellow',-->
<!--            'green'-->
<!--          ],-->
<!--          hoverOffset: 4-->
<!--        }]-->
<!--      },-->
<!--      options: {-->
<!--        responsive: true,-->
<!--        maintainAspectRatio: false,-->
<!--        layout: { padding: { top: 50, bottom: 50 } },-->
<!--        elements: { arc: { borderWidth: 2 } },-->
<!--        animation: { duration: 5000 }-->
<!--      }-->
<!--    }-->
<!--  },-->
<!--  mounted () {-->
<!--    this.renderChart(this.chartData, this.options)-->
<!--  }-->
<!--}-->
<!--</script>-->

<!-- 버블 -->
<!--<script>-->

<!--import { Bubble } from 'vue-chartjs'-->

<!--export default {-->
<!--  extends: Bubble,-->
<!--  data () {-->
<!--    return {-->
<!--      datacollection: {-->
<!--        labels: ['Data'],-->
<!--        datasets: [-->
<!--          {-->
<!--            label: "ㅇㅇ",-->
<!--            backgroundColor: '#f87979',-->
<!--            pointBackgroundColor: 'white',-->
<!--            borderWidth: 1,-->
<!--            pointBorderColor: '#249EBF',-->
<!--            data: [-->
<!--              {-->
<!--                x: 100,-->
<!--                y: 0,-->
<!--                r: 10,-->
<!--              },-->
<!--              {-->
<!--                x: 60,-->
<!--                y: 30,-->
<!--                r: 20-->
<!--              },-->
<!--              {-->
<!--                x: 40,-->
<!--                y: 60,-->
<!--                r: 25-->
<!--              },-->
<!--              {-->
<!--                x: 80,-->
<!--                y: 80,-->
<!--                r: 50-->
<!--              },-->
<!--              {-->
<!--                x: 20,-->
<!--                y: 30,-->
<!--                r: 25-->
<!--              },-->
<!--              {-->
<!--                x: 0,-->
<!--                y: 100,-->
<!--                r: 5-->
<!--              }-->
<!--            ]-->
<!--          }-->
<!--        ]-->
<!--      },-->
<!--      options: {-->
<!--        scales: {-->
<!--          yAxes: [{-->
<!--            ticks: {-->
<!--              beginAtZero: true-->
<!--            },-->
<!--            gridLines: {-->
<!--              display: true-->
<!--            }-->
<!--          }],-->
<!--          xAxes: [{-->
<!--            ticks: {-->
<!--              beginAtZero: true,-->
<!--              fontSize : 40,-->
<!--            },-->
<!--            gridLines: { // 세로-->
<!--              display: true-->
<!--            },-->
<!--          }]-->
<!--        },-->
<!--        // legend: {-->
<!--        //   display: false-->
<!--        // },-->
<!--        tooltips: {-->
<!--          enabled: true,-->
<!--          mode: 'single',-->
<!--          callbacks: {-->
<!--            label: (tooltipItems) => {-->
<!--              return tooltipItems.yLabel + '명'; // 가공-->
<!--            }-->
<!--          }-->
<!--        },-->
<!--        // responsive: true,-->
<!--        // maintainAspectRatio: false,-->
<!--        // height: 100-->
<!--      }-->
<!--    }-->
<!--  },-->
<!--  mounted () {-->
<!--    // this.chartData is created in the mixin-->
<!--    this.renderChart(this.datacollection, this.options)-->
<!--  }-->
<!--}-->
<!--</script>-->

<!-- 반응형? -->
<!--<script>-->
<!--import { Line, mixins } from 'vue-chartjs'-->
<!--const { reactiveProp } = mixins-->

<!--export default {-->
<!--  extends: Line,-->
<!--  mixins: [reactiveProp],-->
<!--  props: ['options'],-->
<!--  mounted () {-->
<!--    // this.chartData is created in the mixin.-->
<!--    // If you want to pass options please create a local options object-->
<!--    this.renderChart(this.chartData, this.options)-->
<!--  }-->
<!--}-->
<!--</script>-->
