<template>
  <form action="" class="form">
    <h1>Todo List App</h1>
    <ul>
      <contentTodoList></contentTodoList>
    </ul>
    <p>total list is complete:0</p>
  </form>
</template>
<script>
import contentTodo from "./contentTodo.vue";
export default {
  components: {
    contentTodoList: contentTodo,
  },
};
</script>
