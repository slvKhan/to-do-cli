<template>
  <div id="app">
    <button class="first" @click="inc">+</button>
    <button class="second" @click="dec">-</button>
    <button class="hide" @click="toggle">toggle</button>
    <template v-if="show">
      {{ counter }}
    </template>
    <br>
    <div class="app-4">
      <ol>
        <li v-for="todo in todos" :key="todo.id">
          {{ todo.text }}
        </li>
      </ol>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      counter: 0,
      show: true,
      todos: [
        { text: 'cat', id: 1 },
        { text: 'cat1', id: 2 },
        { text: 'cat2', id: 3 },
      ],
    };
  },
  methods: {
    toggle() {
      this.show = !this.show;
    },
    inc() {
      this.counter += 1;
    },
    dec() {
      this.counter -= 1;
    },
  },
};
</script>

<style>

</style>
