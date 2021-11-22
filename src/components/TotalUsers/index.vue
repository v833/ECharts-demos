<template>
  <common-card title="累计用户数" value="1,081,014">
    <template>
      <v-chart :option="getOptions()" />
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
  methods: {
    getOptions() {
      return {
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
            layout: "cover",
          },
          {
            type: "bar",
            stack: "总量",
            data: [250],
            itemStyle: {
              color: "#eee",
            },
            layout: "cover",
          },
        ],
        grid: {
          top: 0,
          bottom: 0,
          left: 0,
          right: 0,
        },
      };
    },
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
