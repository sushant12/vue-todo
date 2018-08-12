<template>
  <div id="todo-list">
    <ul>
      <todo-list-item v-for="todo in todos" :key='todo.index' :text='todo.text'/>
    </ul>
  </div>
</template>

<script>
import TodoListItem from './TodoListItem'

export default {
  components: {
    TodoListItem
  },
  props: {
    todos: {
      type: Array
    }
  }
};
</script>

<style scoped>

</style>
