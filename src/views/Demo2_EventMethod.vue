<template>
  <div app="demo2">
    <h1>Demo2: Event Method</h1>
    <button v-on:click="clickMe">Click me</button>
    <button @click="clickMe2('Welcome to VueJS')">Click me2</button>
    <button @click="clickMe2('Welcome to KongKang')">Click me3</button>
    <h3>{{ getTimestamp() }}</h3>
  </div>
</template>

<script>
export default {
  name: "Demo2",
  mounted() {
    this.initial();
  },
  methods: {
    initial() {
      console.log("Initial");
    },
    clickMe() {
      alert("Hi");
    },
    clickMe2(message) {
      alert(message);
    },
    getTimestamp() {
      return Date();
    },
  },
};
</script>

<style></style>
