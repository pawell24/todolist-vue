<template>
  <Form @submit-form="handleSumbitForm" />
  <ul>
    <ToDoItem
      v-for="task in tasks"
      :key="task.id"
      :task="task"
      @remove-task="handleRemoveTask"
    />
  </ul>
</template>

<script>
import Form from "./components/Form.vue";
import ToDoItem from "./components/Todo.vue";

export default {
  name: "App",
  components: { Form, ToDoItem },
  data: () => {
    return {
      tasks: [],
    };
  },
  methods: {
    handleSumbitForm(obj) {
      this.tasks.push(obj);
    },
    handleRemoveTask(id) {
      this.tasks = this.tasks.filter((task) => task.id != id);
    },
  },
};
</script>

<style></style>
