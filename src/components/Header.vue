<template>
  <header>
    <h1>{{ title }}</h1>
    <br>
    <!-- <Button
      @toggle-add-task="$emit('toggle-add-task')"
      :text="showAddTask?'Close':'Add task'"
      color="purple"
    /> -->
  </header>
  <Button
      @toggle-add-task="$emit('toggle-add-task')"
      :text="showAddTask?'Close':'Add task'"
      color="red"
    />
    <br>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean,
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
Button{
    margin-left: 50px;
}
</style>
