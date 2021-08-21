<template>
  <div id="app" class="container">
    <ToDo></ToDo>
  </div>
</template>

<script>
import ToDo from './components/ToDoApp.vue'

export default {
  name: 'App',
  components: {
    ToDo
  }
}
</script>

<style lang="scss">
#app {
  display: grid;
  place-items: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 500px;
}

li {
  text-align: left;
}

.delete-button {
  background: red;
  border: none;
  color: white;
  border-radius: 10%;
}
</style>
