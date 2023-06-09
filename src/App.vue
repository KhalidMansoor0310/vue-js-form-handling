<template>
  <AppForm msg="Welcome to Your Vue Js Form Handling" />
</template>

<script>
import AppForm from "./components/AppForm.vue";

export default {
  name: "App",
  components: {
    AppForm,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

#app {
  font-family: "Merienda", Helvetica, Arial;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
