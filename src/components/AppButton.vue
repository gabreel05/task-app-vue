<template>
  <button @click="clickButton">{{ data }}</button>
</template>

<script>
export default {
  name: "AppButton",
  props: {
    textButton: {
      type: String,
      required: true,
    },
    clickButton: {
      type: Function,
      required: true,
    },
  },
  data() {
    return {
      data: this.textButton,
    };
  },
};
</script>

<style>
button {
  border: none;
  outline: none;
  background-color: #66cc;
  border-radius: 5px;
  padding: 15px;
  font-size: 14px;
  font-weight: bold;
  color: #eee;
  margin: 10px;
}

button:hover {
  background-color: #eee;
  color: #777;
  cursor: pointer;
}
</style>
