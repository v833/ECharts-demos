<template>
  <common-card title="累计销售额" value="￥32,039,165">
    <div class="compare-wrapper">
      <div class="compare">
        <span>日同比：</span>
        <span class="emphasis">7.33%</span>
        <div class="increase"></div>
      </div>
      <div class="compare">
        <span>月同比：</span>
        <span class="emphasis">4.23%</span>
        <div class="decrease"></div>
      </div>
    </div>
    <template #footer>
      <span>昨日销售额：</span>
      <span class="emphasis">￥30,300,300</span>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from "../../mixins/CommonCardMixin";
export default {
  mixins: [commonCardMixin],
};
</script>

<style lang="scss">
.compare-wrapper {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  .compare {
    height: 50%;
    // background-color: yellow;
    margin-top: 3px;
    display: flex;
    align-items: center;
  }
}
span {
  font-size: 12px;
}
</style>