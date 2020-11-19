<template>
  <div id="app">
    <Header />
    <router-view/>
    <DraggableArea />
  </div>
</template>

<script>
import Header from './components/layout/Header'
import DraggableArea from './components/layout/DraggableArea'
export default {
  name:"app",
  components: {
    Header,
    DraggableArea
  }
}
</script>

<style>
</style>
