<template>
  <div id="demo1">
    <h1>Demo1: V-model</h1>
    <!-- mvvm -->
    <input v-model="message" type="text" placeholder="Enter your message" />
    <div>{{ message }}</div>
    <button @click="message = ''">Reset</button>
  </div>
</template>

<script>
export default {
  name: "Demo1",
  data() {
    return {
      message: "",
    };
  },
};
</script>

<style>
button {
  margin-top: 10px;
}
</style>
