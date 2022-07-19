<template>
  <div id="app">
    <AppHeader />
    <AppButton :textButton="textButton" :click="addTask" />
    <AddTaskForm :isShown="isShown" />
    <AppTasks :tasks="tasks" :isShown="!isShown" />
  </div>
</template>

<script>
import AddTaskForm from "./components/AddTaskForm.vue";
import AppButton from "./components/AppButton.vue";
import AppHeader from "./components/AppHeader.vue";
import AppTasks from "./components/AppTasks.vue";
export default {
  components: { AppHeader, AppTasks, AddTaskForm, AppButton },
  name: "App",
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: "Make coffe",
          completed: false,
        },
        {
          id: 2,
          title: "Study Vue.JS",
          completed: false,
        },
      ],
      isShown: false,
      textButton: "Add Task",
    };
  },
  methods: {
    addTask() {
      this.isShown = !this.isShown;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
