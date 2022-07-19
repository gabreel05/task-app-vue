<template>
  <div
    :style="{
      display: isShown ? 'block' : 'none',
      visibility: isShown ? 'visible' : 'hidden',
    }"
    id="add_task__form"
  >
    <h1>Add Task</h1>
  </div>
</template>

<script>
export default {
  name: "AddTaskForm",
  props: {
    isShown: {
      type: Boolean,
      required: true,
    },
  },
};
</script>
