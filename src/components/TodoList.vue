<template>
  <div>
    <div v-for="(action, i) in actions" :key="i">
       <TodoItem 
       :action = 'action'
       @delet = 'delet'
       />
       </div>
      </div>
</template>

<script>
import TodoItem from './TodoItem';


export default {
  name: 'Todolist',
    props: {
    actions: {
      type: Array,
      required: true,
      default: null
    },
 
  },
  components: {
    TodoItem,
  },
  methods: {
    delet(event){
       this.$emit('delet-word', event);
        console.log(event)
    }
    },
}
</script>

<style>

</style>