<template>
  <div class="center">
    <input type="text" 
    v-model="text"
     />
    <button
      @click="addTodolist"
      v-show="actions.length < 10"
    >Add new todo</button>
    </div>
</template>

<script>
export default {
  name: "AddTodo",
  props: {
    actions: {
      type: Array,
      required: true,
      default: null
    },
 
  },
  data() {
    return {
      text: "",
      };
  },
  methods: {
    addTodolist() {
      if (this.text.length > 0){
      this.$emit('add-words', this.text);
      this.text = "";
      }
    },
  
  },
};
</script>

<style>
div {
  text-align: center;
}
</style>
