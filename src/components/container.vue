<template>
  <div class="container"
       @dragover.prevent
       @dragenter="enter"
       @dragleave="leave"
       @drop="drop"
  >
    <slot/>
  </div>
</template>

<script>
  export default {
    name: "container",
    data() {
      return {
        classes: ''
      }
    },
    methods: {
      enter(){
        // console.log('enter')
      },
      leave(){
        // console.log('leave')
      },
      drop(){
        console.log(document.querySelector('#memes'))
        console.log(this.$el.append(document.querySelector('#memes')))
      }
    }
  }
</script>

<style lang="scss">
.container {
  width: 300px;
  height: 300px;
  border: 1px solid black;
}
</style>
