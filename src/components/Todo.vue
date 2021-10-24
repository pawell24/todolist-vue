<template>
  <li>
    <div>
      <h2>{{ task.title }}</h2>
      <p>{{ task.description }}</p>
      <p>{{ task.date }}</p>
      <button @click="removeToDoItem">Remove</button>
    </div>
  </li>
</template>

<script>
export default {
  name: "Todo",
  props: {
    task: Object,
  },
  methods: {
    removeToDoItem() {
      this.$emit("remove-task", this.task.id);
    },
  },
};
</script>

<style></style>
