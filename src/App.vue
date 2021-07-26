<script>
import TodoItem from './components/TodoItem.vue';

export default {
  name: 'App',
  data() {
    return {
      todos: [
        { id: 1, title: 'Купить хлеб', completed: false },
        { id: 2, title: 'Купить яйца', completed: false },
        { id: 3, title: 'Купить молоко', completed: false },

      ],

    };
  },
  methods: {
  },
  components: {
    TodoItem,
  },
};
</script>

<template>
    <div id="app">
        <ol>
            <TodoItem v-for="todo in todos" :key="todo.id" :title="todo.title"></TodoItem>
        </ol>
    </div>
</template>

<style>
</style>
