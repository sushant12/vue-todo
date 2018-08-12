<template>
  <div id="app">
    <base-input v-model='newTodo' placeholder='Add Todo' @itemAdded='addTodo'/>
    <todo-list :todos='todos'/>
  </div>
</template>

<script>
import BaseInput from './components/BaseInput.vue'
import TodoList from './components/TodoList.vue'

export default {
  components: {
    BaseInput,
    TodoList
  },
  data(){
    return {
      newTodo: '',
      todos: []
    }
  },
  methods: {
    addTodo(){
      if(this.newTodo.trim().length == 0){
        return
      }
      this.todos.push({text: this.newTodo, completed: false});
      this.newTodo = ''
    }
  }
};
</script>

<style>

</style>
