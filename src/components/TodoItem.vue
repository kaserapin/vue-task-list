<template>
  <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
    <p>
      <span class="left">
        <input type="checkbox" @change="todoComplete">
        {{todo.title}}
      </span>
      <span class="right">
        <button @click="$emit('del-todo', todo.id)" class="del">Delete</button>
      </span>
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    todoComplete() {
      this.todo.completed = !this.todo.completed;
    }
  }
};
</script>
<style scoped>
p {
  display: flex;
}
.left {
  flex: 9;
}
.right {
  flex: 3;
}
.todo-item {
  background: #fff;
  padding: 10px;
  border-bottom: 1px solid #ccc;
}
.is-complete {
  text-decoration: line-through;
}

.del {
  background-color: #ff0000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  float: right;
}
input[type="checkbox"] {
  margin-right: 25px;
}
</style>
