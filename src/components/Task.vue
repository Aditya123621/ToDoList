<template>
  <div @dblclick="$emit('toggle-reminder',task.id)" :class="[task.reminder ? 'reminder' : '', 'task']">
    <p>{{ task.day }}</p>
    <hr>
    <h3>
      {{ task.text }}
      
    </h3>
    <button class="btn" style="background-color: greenyellow;color: black;" @click="$emit('delete-task',task.id)">Delete</button>
  </div>
</template>

<script>
export default {
  name: "Task",
  props: {
    task: Object,
  },
};
</script>

<style scope>
.fa {
  color: red;
}
.fa {
  margin: 0px 30px;
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
  background-color: darkturquoise;
}
.task.reminder {
  border-left: 5px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.btn{
    background-color: greenyellow;
}
</style>
