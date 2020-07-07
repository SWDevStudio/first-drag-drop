<template>
<!--  draggable - принимает булевое значение, при true позволяет перетаскивать элемент при помощи drag&drop-->
  <div class="content" :draggable="draggable" @dragstart="start" @dragend="end" id="memes" >
    <h1>Какие то данные</h1>
    <p>информация о данных</p>
  </div>
</template>

<script>
  export default {
    name: "v-content",
    props: {
      draggable: Boolean
    },
    methods: {
      // Метод срабатывает когда мы начинаем перетаскивать элемент
      start(){
        console.log('start')
      },
      // метод срабатывает когда мы заканчиваем перетаскивать элемент
      end(){
        console.log('end')
      },


    }
  }
</script>

<style lang="scss">
  .content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100%;
    align-items: center;

  }
</style>
