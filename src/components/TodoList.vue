<template>
<div>
  TodoList
  <ul>
    <li v-for="todo in todos" :key="todo.index">
      {{todo.title}}
    </li>
  </ul>
</div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'TodoList',
  data() {
    return {
      todos: [],
      errors: [],
    };
  },
  mounted() {
    axios.get('https://jsonplaceholder.typicode.com/todos').then(
      (results) => {
        this.todos = results.data;
        console.log(results);
      },
    ).catch((error) => {
      this.errors.push(error);
    });
  },
};
</script>

<style scoped>

</style>
