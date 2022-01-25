<script>
import { Bubble, mixins } from 'vue-chartjs'
const { reactiveProp } = mixins

export default {
  extends: Bubble,
  mixins: [reactiveProp],
  props: ['options'], // 의미를 모르겠다
  async mounted () {
    // this.chartData is created in the mixin.
    // If you want to pass options please create a local options object
    this.$nextTick(() => {
      this.renderChart(this.chartData, this.options)
    })
  }
}
</script>
