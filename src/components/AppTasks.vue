<template>
  <div v-show="isShown" id="app__tasks">
    <ul>
      <li v-for="task in tasks" v-bind:key="task.id">
        <input type="checkbox" v-model="task.completed" />
        <span v-text="task.title"></span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "AppTasks",
  props: {
    tasks: {
      type: Array,
      required: true,
    },
    isShown: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style>
#app__tasks ul {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#app__tasks ul li {
  width: 25%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin: 10px;
  padding: 10px;
  border: 1px solid #7159c1;
  border-radius: 5px;
}
</style>
