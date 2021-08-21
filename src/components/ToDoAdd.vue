<template>
  <div>
    <h2 class="my-4">Crea una nueva tarea</h2>
    <label class="mr-2">Tarea:</label>
    <input type="text" placeholder="Ingrese nueva tarea" v-model="newToDo" />
    <button @click="createToDo()">Crear</button>
  </div>
</template>

<script>
export default {
  name: 'ToDoAdd',
  data: () => ({
    newToDo: ''
  }),
  methods: {
    createToDo() {
      this.$emit('new-todo', this.newToDo)
      this.newToDo = ''
    }
  }
}
</script>

<style></style>
