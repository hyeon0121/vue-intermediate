<template>
  <div class="inputBox shadow">
    <input type="text" v-model="newTodoItem" @keyup.enter="addTodo">
    <span class="addContainer" @click="addTodo">
      <i class="fas fa-plus addBtn "></i>
    </span>
  </div>
</template>

<script>

export default {
  data: function() {
    return {
      newTodoItem : ""
    }
  },
  methods: {
    addTodo() {
      localStorage.setItem(this.newTodoItem, this.newTodoItem);
      this.clearInput();
    },
    clearInput() {
      this.newTodoItem = "";
    }
  }

}
</script>

<style scoped>

</style>