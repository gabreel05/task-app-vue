<template>
  <div v-show="isShown" id="add_task__form">
    <div id="add_task__form__items">
      <h1>Add Task</h1>
      <input type="text" placeholder="Task Title" v-model="title" />
      <AppButton :textButton="textButton" :clickButton="addTask" />
    </div>
  </div>
</template>

<script>
import AppButton from "./AppButton.vue";
export default {
  components: { AppButton },
  name: "AddTaskForm",
  props: {
    isShown: {
      type: Boolean,
      required: true,
    },
    taskList: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      textButton: "Add",
      title: "",
      tasks: this.taskList,
    };
  },
  methods: {
    addTask() {
      this.tasks.push({
        id: 4,
        title: this.title,
        completed: false,
      });
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
  margin: 10px;
}

#add_task__form #add_task__form__items {
  border: 1px solid #66cc;
  border-radius: 5px;
  width: 25%;
  padding: 10px;
}

#add_task__form #add_task__form__items input {
  border: none;
  outline: none;
  background-color: #eee;
  padding: 15px;
  border-radius: 15px;
  margin-right: 5px;
}
</style>
