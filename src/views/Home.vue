<template>
  <div class="home">
    <Top-view />
    <Sales-view />
    <Bottom-view />
    <Map-view />
  </div>
</template>

<script>
import TopView from "../components/TopView";
import MapView from "../components/MapView";
import BottomView from "../components/BottomView";
import SalesView from "../components/SalesView";

export default {
  name: "Home",
  components: {
    TopView,
    MapView,
    BottomView,
    SalesView,
  },
};
</script>

<style lang="scss">
.home {
  box-sizing: border-box;
  height: 100%;
  width: 100%;
  padding: 20px;
  background-color: #eee;
}
</style>