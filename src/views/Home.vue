<template>
  <div class="home">
    report
    <Top-view />
    <Map-view />
    <Button-view />
    <Sales-view />

  </div>
</template>

<script>
import TopView from '../components/TopView'
import MapView from '../components/MapView'
import ButtonView from '../components/ButtonView'
import SalesView from '../components/SalesView'


export default {
  name: 'Home',
  components: {
    TopView,
    MapView,
    ButtonView,
    SalesView
  }
}
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