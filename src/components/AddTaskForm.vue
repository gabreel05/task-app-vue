<template>
  <div v-show="isShown" id="add_task__form">
    <div id="add_task__form__items">
      <h1>Add Task</h1>
    </div>
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

<style>
#add_task__form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

#add_task__form__items {
  border: 1px solid #66cc;
  border-radius: 5px;
  width: 50%;
}
</style>
