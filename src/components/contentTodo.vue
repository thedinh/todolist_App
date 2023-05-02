<template>
  <input type="text" class="textContent" v-model="textContent" />
  <button class="addbtn" @click="getDataInput(textContent)">
    Add todo List
  </button>
  <li v-for="(todo, index) in todos" :key="todo.idtask" class="content__li">
    <input type="checkbox" v-model="todo.isComplete" @click="checked" />
    <p :class="{ active: todo.isComplete }">{{ todo.taskContent }}</p>
    <button @click="DeleteTodo(index)">x</button>
  </li>
  <p class="total">total todoList need to do: {{ todos.length }}</p>
</template>
<script>
export default {
  data() {
    return {
      count: 0,
      nextContent: "",
      todos: [
        {
          idtask: 1,
          taskContent: "do homework",
          isComplete: false,
        },
        {
          idtask: 2,
          taskContent: "do gym",
          isComplete: false,
        },
        {
          idtask: 3,
          taskContent: "do swimming",
          isComplete: false,
        },
        {
          idtask: 4,
          taskContent: "play football",
          isComplete: false,
        },
        {
          idtask: 5,
          taskContent: "code webapp",
          isComplete: false,
        },
      ],
    };
  },
  methods: {
    getDataInput: function (textContent) {
      this.todos.push({
        idtask: 6,
        taskContent: textContent,
        isComplete: false,
      });
    },
    checkedData: function () {
      console.log(this.todos.isComplete);
    },
    DeleteTodo: function (index) {
      this.todos.splice(index, 1);
    },
  },
};
</script>
