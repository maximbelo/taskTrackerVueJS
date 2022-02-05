<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      text="Add Task"
      color="green"
      @toggle-add-task="$emit('toggle-add-task')"
    />
  </header>
</template>

<script>
import Button from "./Button";

export default {
  name: "Header",
  // Props can be defined as an array or object -> If added as an object we define the type and we can also define a default value
  props: {
    title: String,
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
