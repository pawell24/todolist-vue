<template>
  <Form @submit-form="handleSumbitForm" />
  <ul>
    <li v-for="task in tasks" :key="task.title">{{ task.title }}</li>
  </ul>
</template>

<script>
import Form from "./components/Form.vue";
export default {
  name: "App",
  components: { Form },
  data: () => {
    return {
      tasks: [],
    };
  },
  methods: {
    handleSumbitForm(obj) {
      this.tasks.push(obj);
      console.log(this.tasks);
    },
  },
};
</script>

<style></style>
