<template>
  <div id="app">
    <TodoList v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
import TodoList from './components/TodoList'

export default {
  name: 'app',
  data(){
    return {
      todos: ['Зарядка', 'Завтрак', 'Занятия', "Обед"]
    }
  },
  components: {
    TodoList
  },
  methods: {
    deleteTodo(index){
      this.todos.splice(index, 1);
    }
  }
}
</script>

<style>
body{
  background-color: lightblue;
}
.list{
  height: 500px;
  width: 350px;
  align-items: center;
}
.title{
  background-color: blueviolet;
  color: white;
  text-align: center;
  padding: 1px;
  border-radius: 15px;
}
.doings{
  height: auto;
  width: 320px;
  background-color: white;
  padding: 15px;
  margin-top: 15px;
  border-radius: 20px;
}
</style>