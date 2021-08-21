<template>
  <div>
    <h3 class="my-4">Lista de Tareas</h3>
    <ul>
      <li class="my-2" v-for="(ToDo, $index) in existingToDo" :key="$index">
        {{ $index + 1 }}: {{ ToDo.text }}
        <button class="delete-button ml-5" @click="deleteToDo($index)">
          Eliminar
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ToDoList',
  props: {
    existingToDo: { type: Array, required: true }
  },
  methods: {
    deleteToDo($index) {
      this.$emit('delete-todo', $index)
    }
  }
}
</script>

<style></style>
