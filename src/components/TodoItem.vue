<template>
  <div>
  <span>
    {{action}}
    <button @click="remove">Remove</button>
  </span>
    </div>
</template>

<script>
export default {
  name: "TodoItem",
   props: {
    action: {
      type: String,
      default: null
    },
   },
  data() {
    return {
      
      };
  },
  methods: {
       remove() {
      this.$emit('delet', this.action);
    },
  }
   }

</script>