<template>
  <common-card title="累计订单量" value="2,157,420">
    <template>
      <v-chart :option="getOptions()" />
    </template>

    <template #footer>
      <span>昨日订单量：</span>
      <span class="emphasis">2,000,000</span>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from "../../mixins/CommonCardMixin";
export default {
  mixins: [commonCardMixin],
  data() {
    return {}
  },
  methods: {
    getOptions() {
      return {
        xAxis: {
          type: "category",
          show: false,
          boundaryGap: false,
        },
        yAxis: {
          show: false,
        },
        series: [
          {
            type: "line",
            data: [
              510, 540, 520, 620, 510, 540, 520, 620, 510, 540, 520, 620, 510,
              540, 520, 620, 510, 540, 520, 620,
            ],
            areaStyle: {
              color: "purple",
              smooth: true,
            },
            lineStyle: {
              width: 0,
            },
            itemStyle: {
              opacity: 0,
            },
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
</style>