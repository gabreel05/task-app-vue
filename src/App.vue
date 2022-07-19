<template>
  <div id="app">
    <AppHeader />
    <button @click="addTask" type="button">Add Task</button>
    <AddTaskForm :isShown="isShown" />
    <AppTasks :tasks="tasks" />
  </div>
</template>

<script>
import AddTaskForm from "./components/AddTaskForm.vue";
import AppHeader from "./components/AppHeader.vue";
import AppTasks from "./components/AppTasks.vue";
export default {
  components: { AppHeader, AppTasks, AddTaskForm },
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

#app button {
  border: none;
  outline: none;
  background-color: #66cc;
  border-radius: 5px;
  padding: 15px;
  font-size: 14px;
  font-weight: bold;
  color: #eee;
  margin-top: 5px;
  margin-bottom: 5px;
}

#app button:hover {
  background-color: #eee;
  color: #777;
  cursor: pointer;
}
</style>
