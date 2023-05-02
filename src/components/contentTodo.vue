<template>
  <div>
    <ul>
      <li v-for="(todo, index) in todos" :key="todo.idtask">
        <input type="checkbox" name="" :class="index" />
        <a href="#">{{ todo.taskContent }}</a>
        <button>x</button>
      </li>
    </ul>
  </div>
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
      ],
    };
  },
};
</script>
