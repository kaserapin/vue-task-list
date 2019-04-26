<template>
  <div class="about">
    <h1>{{title}}</h1>
    <p>{{description}}</p>
  </div>
</template>

<style scoped>
.about {
  width: 80%;
  margin: auto;
  text-align: center;
}
h1 {
  margin-bottom: 50px;
}
</style>

<script>
export default {
  data() {
    return {
      title: "About",
      description:
        "This app created using Vue.js. JSONPlaceholder is used as a backend api."
    };
  }
};
</script>


