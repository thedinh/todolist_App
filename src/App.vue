<template>
  <TodoListContent></TodoListContent>
</template>

<script>
import TodoList from "./components/TodoList.vue";
export default {
  name: "App",
  components: {
    TodoListContent: TodoList,
  },
};
</script>
