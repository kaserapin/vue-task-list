<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add todo">
      <input type="submit" value="Submit" class="btn">
    </form>
  </div>
</template>

<script>
// import uuid from "uuid";

export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    addTodo() {
      const newTodo = {
        title: this.title,
        completed: false
      };
      // send up to parent
      this.$emit("add-todo", newTodo);

      this.title = "";
    }
  }
};
</script>

<style scoped>
form {
  display: flex;
  width: 80%;
  margin: 100px auto 0;
}
input[type="text"] {
  flex: 10;
  padding: 15px 20px;
  box-sizing: border-box;
}

input[type="submit"] {
  flex: 2;
  background-color: green;
}
</style>

