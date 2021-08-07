<template>
  <div id="demo10">
    <h1>Demo10: LifeCycle Hooks</h1>
    <span>{{ counter }}</span>
    <br />
    <button @click="add">Change</button>
  </div>
</template>

<script>
export default {
  name: "Demo10",
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    add() {
      this.counter++;
    },
  },
  beforeCreate() {
    console.log("beforecreated");
  },
  created() {
    console.log("created");
  },
  mounted() {
    console.log("mounted");
  },
  beforeUpdate() {
    console.log("beforeUpdate");
  },
  updated() {
    console.log("updated");
  },
  beforeDestroy() {
    console.log("beforeDestroy");
  },
  destroyed() {
    console.log("destroyed");
  },
};
</script>

<style></style>
