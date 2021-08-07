<template>
  <div id="demo12">
    <h1 ref="title">Waiting for title</h1>
    <input ref="input1" type="text" placeholder="This will be focused" />
  </div>
</template>

<script>
export default {
  name: "Demo12",
  mounted() {
    this.$refs["title"].textContent = "Demo 12: Ref";
    this.$refs["input1"].focus();
    this.$refs["input1"].value = "1234";
  },
};
</script>

<style></style>
