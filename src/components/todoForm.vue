<template>
  <Card>
    <h1 class="title">Todo List | Vue.JS</h1>
    <InputText class="field" />
    <Btn class="add-btn" />
  </Card>
</template>

<script>
  import Card from "./card"
  import InputText from "./inputText"
  import Btn from "./btn"
  export default {
    name: 'TodoForm',
    components: {
      Card,
      InputText,
      Btn,
    }
  }
</script>

<style scoped>
  .title {
    font-size: 27px;
    text-align: center;
    margin-bottom: 1em;
  }

  .field {
    display: block;
    width: 100%;
    margin-bottom: 10px;
  }

  .add-btn {
    display: block;
    width: 100%;
  }
</style>