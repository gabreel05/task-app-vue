<template>
  <div id="app__header">
    <h1>Tasks</h1>
    <input type="text" placeholder="Search" />
  </div>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style>
#app__header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
  background: #66cc;
  color: #f5f5f5;
}

#app__header input {
  border: none;
  outline: none;
  border-radius: 5px;
  padding: 15px;
  margin-right: 2.5px;
}

#app__header input:focus {
  border: none;
  outline: none;
}
</style>
