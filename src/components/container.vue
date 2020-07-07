<template>
<!--  Все @ это события ванильного JS проверенно-->
  <div class="container"
       @dragover.prevent="over"
       @dragenter="enter"
       @dragleave="leave"
       @drop="drop"
  >
<!--    Про slot читай в документации vue-->
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
    // this --> возвращает Vue компонент над которым занесен блок
    // this.$el --> возвращает элемент над которым занесен блок
    methods: {
      // данный метод срабатывает постоянно когда мы держим v-content над элементом
      over() {

      },
      // данный метод срабатывает когда мы заносим v-content в элемент
      enter(){
        // console.log('enter')
      },
      // данный метод срабатывает когда мы выносим v-content из элемента
      leave(){
        // console.log('leave')
      },
      // данный метод срабатывает когда отпускаем левую кнопку мыши,
      drop(){
        console.log(document.querySelector('#memes'))
        // append -> добавляет данные в определенный блок, убирая их из блока в котором они были до этого
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
