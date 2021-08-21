<template>
  <div>
    <ToDoAdd @new-todo="createToDo"></ToDoAdd>
    <ToDoList :existingToDo="existingToDo" @delete-todo="deleteToDo"></ToDoList>
  </div>
</template>
<script>
import ToDoList from './ToDoList.vue'
import ToDoAdd from './ToDoAdd.vue'
export default {
  name: 'ToDo',
  components: {
    ToDoList,
    ToDoAdd
  },
  data: () => ({
    existingToDo: []
  }),
  methods: {
    createToDo(newToDo) {
      this.existingToDo.push({
        text: newToDo,
        $index: this.existingToDo.length
      })
    },
    deleteToDo($index) {
      this.existingToDo.splice($index, 1)
    }
  }
}
</script>

<style></style>
