<template>
  <TodoForm />
  <TodoList />
</template>

<script>
  import TodoForm from "./components/todoForm"
  import TodoList from "./components/todoList"
  export default {
    name: 'App',
    components: {
      TodoForm,
      TodoList,
    },
  }
</script>