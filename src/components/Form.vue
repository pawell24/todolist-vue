<template>
  <div>
    <form @submit.prevent="">
      <div class="wrapper">
        <label>Title:<input type="text" v-model="title"/></label><br />
        <label>Description:<textarea v-model="description"/></label><br />
        <label>Date:<input type="date" v-model="date"/></label>
      </div>
    </form></div
></template>

<script>
export default {
  name: "Form",
  data: () => {
    return {
      title: "",
      description: "",
      date: "",
    };
  },
};
</script>

<style scoped>
.wrapper {
  margin: 100px auto;
}
form div {
  width: 20%;
  border: 2px solid black;
  padding: 10px;
  font-family: sans-serif;
}
label {
  display: flex;
  justify-content: space-between;
}
</style>
