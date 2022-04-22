<template>
  <header>
    <h1>Task Tracker</h1>
    <Button @click="addTask()" text="Add Task" color="green" />
    <Button @click="deleteAll()" text="Delete All" color="red" />
  </header>
</template>

<script>
  import Button from "@/components/Button";

  export default {
    name: 'Header',
    components: {
      Button
    },
    methods: {
      deleteAll() {
        this.$emit('delete-all')
      },
      addTask() {
        this.$emit('add-task')
      }
    }
  }
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>