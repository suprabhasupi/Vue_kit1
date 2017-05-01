<template>
<div>
<p>Hello Supi!</p>

<todo-list></todo-list>

</div>
</template>
<script>
import todoList from './components/todoList';
import './styles/style.scss';
import './app.scss';

export default {
	components: {
    todoList
  },
  data: function(){
  	return{

  	}
  }
}

</script>
