<template>
  <li v-for="(todo, index) in todos" :key="todo.idtask">
    <input type="checkbox" name="" :class="index" />
    <a href="#">{{ todo.taskContent }}</a>
    <button>x</button>
  </li>
</template>
<script>
export default {
  data() {
    return {
      todos: [
        {
          idtask: 1,
          taskContent: "do something",
        },
        {
          idtask: 2,
          taskContent: "do something",
        },
        {
          idtask: 3,
          taskContent: "do something",
        },
        {
          idtask: 4,
          taskContent: "do something",
        },
        {
          idtask: 5,
          taskContent: "do something",
        },
      ],
    };
  },
};
</script>
