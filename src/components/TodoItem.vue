<script>
export default {
  name: 'TodoItem',
  props: ['title'],
};
</script>

<template>
    <li>{{ title }}</li>
</template>
