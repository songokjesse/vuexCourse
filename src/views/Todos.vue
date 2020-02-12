<template>
<div>
  <h1>Todos</h1>
  <todo-list></todo-list>
</div>
</template>

<script>
import TodoList from '../components/TodoList.vue';

export default {
  name: 'Todos',
  components: { TodoList },
};
</script>

<style scoped>

</style>
