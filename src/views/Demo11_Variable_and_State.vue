<template>
  <div id="deomo11">
    <h1>Demo11: Normal&State Variable</h1>
    <div>{{ count }}</div>
    <div>{{ Math.random() }}</div>
    <div>{{ "Timestamp :" + this.timestamp }}</div>
    <button @click="timestamp = Date.now()">Update Timestamp</button>
    <button @click="count++">Update Count</button>
  </div>
</template>

<script>
export default {
  name: "Demo11",
  created() {
    //  normal Variable
    this.timestamp = 0;
  },
  mounted() {
    setInterval(() => {
      //   this.count++;
      console.log("Timestamp :" + this.timestamp);
    }, 1000);
  },
  data() {
    return {
      // local state
      count: 0,
    };
  },
};
</script>

<style></style>
