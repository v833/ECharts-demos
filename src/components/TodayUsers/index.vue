<template>
  <common-card title="今日交易用户数" value="81,014">
    <template>
      <div
        id="today-users-chart"
        :style="{ width: '100%', height: '100%' }"
      ></div>
    </template>

    <template #footer>
      <span>退货率: </span>
      <span class="emphasis">5.14%</span>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from "../../mixins/CommonCardMixin";
export default {
  mixins: [commonCardMixin],
  mounted() {
    const chart = this.$echarts.init(document.querySelector('#today-users-chart'))
    chart.setOption({
      color: ['#3398DB'],
      xAxis: {
        type: 'category',
        data: ['00:00','01:00','02:00','03:00','04:00','05:00','06:00','07:00','08:00','09:00'],
        show: false,
      },
      yAxis: {
        show: false
      },
      series: [{
        type: 'bar',
        data: [100, 124, 140,163 ,162 ,134, 127, 109, 174, 163],
        barWidth: '60%'
      }],
      grid: {
        top: 0,
        bottom: 0,
        left:0,
        right: 0
      }
    })
  },
};
</script>

<style lang="scss">
</style>