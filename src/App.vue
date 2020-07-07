<template>
  <div id="app">
    <container><v-content :draggable="true"/></container>
    <container></container>
  </div>
</template>

<script>




import Container from "./components/container";
import vContent from "./components/v-content";
export default {
  name: 'App',
  components: {
    vContent,
    Container
  }
}
</script>

<style lang="scss">
  #app {
    display: flex;
    justify-content: space-between;
    max-width: 1024px;
    margin: 0 auto;
  }
 * {
   margin: 0;
   padding: 0;
   box-sizing: border-box;
 }

  body {
    background: #F3F3F3;
  }

</style>
