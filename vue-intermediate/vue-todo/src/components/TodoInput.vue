<template>
  <div class="inputBox shadow">
    <input type="text" v-model="newToDoItem" v-on:keyup.enter="addTodo">
    <!-- <button v-on:click="addTodo">Add</button> -->
    <span class="addContainer" v-on:click="addTodo">
      <i class="addBtn fas fa-plus"></i>
    </span>
  </div>
</template>

<script>
export default {
data: function() {
  return {
    newToDoItem: ""
  }
},
methods: {
  addTodo: function() {
    if (this.newToDoItem !== '') {
    this.$emit('addTodoItem', this.newToDoItem)
    this.clearInput()
    }
  },
  clearInput: function() {
    this.newToDoItem = ''
  }
}
}
</script>

<style scoped>
input:focus {
  outline: none;
}
.inputBox {
  background: white;
  height: 50px;
  line-height: 50px;
  border-radius: 5px;
}
.inputBox input {
  border-style: none;
  font-size: 0.9rem;
}
.addContainer {
  float: right;
  background: linear-gradient(to right, #6478FB, #8763FB);
  display: block;
  width: 3rem;
  border-radius: 0 5px 5px 0;
}
.addBtn {
  color: white;
  vertical-align: middle;
}
.closeModalBtn {
  color: #42b983;
}
</style>