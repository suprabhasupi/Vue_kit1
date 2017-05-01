<template>
<div id="todo">
  <input
    v-model="newTodoText"
    v-on:keyup.enter="addNewTodo"
    placeholder="Add a todo"
  >
  <ul>
    <li 
    v-for="(todo, index) in todos"
    v-bind:key="todo"
    v-bind:title="todo"
    >
    <!-- todos.splice(index, 1); -->
      {{index}} {{ todo }}
    <button @click="remove(index)">X</button>
    </li>
  </ul>
</div>
</template>

<script type="text/javascript">
import todoList from './todo-list.scss'
export default {
  name: 'todo-list',
  props: ['title'],
  data: function() {
    return {
     newTodoText: '',
     todos: [
      'Do the dishes',
      'Take out the trash',
      'Mow the lawn'
    ]

    };
  },
  methods:{
    addNewTodo: function(){
      this.todos.push(this.newTodoText)
      this.newTodoText = ''
    },
    remove: function(index){
      this.todos.splice(index, 1)
    }
  }
}
</script>