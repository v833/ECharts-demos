<template>
  <common-card title="累计用户数" value="1,081,014">
    <template>
      <div
        id="total-users-chart"
        :style="{ width: '100%', height: '100%' }"
      ></div>
    </template>
    <template #footer>
      <div class="total-users-footer">
        <span>日同比：</span>
        <span class="emphasis">8.73%</span>
        <div class="increase"></div>
        <span class="mouth">月同比：</span>
        <span class="emphasis">10.22%</span>
        <div class="decrease"></div>
      </div>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from "../../mixins/CommonCardMixin";
export default {
  mixins: [commonCardMixin],
  mounted() {
    const chart = this.$echarts.init(
      document.querySelector("#total-users-chart")
    );
    chart.setOption({
      xAxis: {
        type: "value",
        show: false,
      },
      yAxis: {
        type: "category",
        show: false,
      },
      series: [
        {
          type: "bar",
          stack: "总量",
          data: [200],
          barWidth: 10,
          itemStyle: {
            color: "#45c946",
          },
        },
        {
          type: "bar",
          stack: "总量",
          data: [250],
          itemStyle: {
            color: "#eee",
          },
        },
      ],
      grid: {
        top: 0,
        bottom: 0,
        left: 0,
        right: 0,
      },
    });
  },
};
</script>

<style lang="scss">
.total-users-footer {
  display: flex;
  align-items: center;
  .mouth {
    margin-left: 10px;
  }
}
</style>
