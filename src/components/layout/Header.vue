<template>
  <header class="header">
    <h1>Task list</h1>
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.header {
  background: #fff;
  color: #333;
  text-align: center;
  padding: 10px;
  margin-bottom: 50px;
  box-shadow: 0 0 10px #666;
}

.header a {
  color: #333;
  padding-right: 5px;
  text-decoration: none;
}

h1 {
  margin-bottom: 10px;
}
</style>

