<template>
  <div>
    <AddTodo
    :actions = "actions"
    @add-words = "addWords"
    />
    <TodoList
    :actions = "actions"
    @delet-word = 'deletWord'
    />
      </div>
</template>

<script>
import AddTodo from './components/AddTodo';
import TodoList from './components/TodoList';


export default {
  name: 'App',
  data() {
    return {
      actions: ["Go to the shop", "Go for a walk", "Make a coffe"],
      ac: 'фваіва'
      
      };
  },
  components: {
    AddTodo,
    TodoList
  },
   methods: {
    addWords(event){
      this.actions.push(event);
      console.log(event)
    },
    deletWord(event){
      let index = this.actions.findIndex(action => action === event);
      this.actions.splice(index, 1);
    }
    },
    

}
</script>

<style>

</style>
