<template>
  <div id="demo8">
    <h1>Demo8: Condition</h1>
    <div v-if="type == 'A'">
      I am A
    </div>
    <div v-else-if="type == 'B'">
      I am B
    </div>
    <div v-else-if="type == 'C'">
      I am C
    </div>
    <div v-else>
      Not A/B/C
    </div>
    <div v-if="isShow">
      Bling 1
    </div>
    <div v-else>
      Bling 2
    </div>
    <div v-show="isShow">
      Bling V-Show
    </div>
  </div>
</template>

<script>
export default {
  name: "Demo8",
  mounted() {
    setInterval(() => {
      this.isShow = false;
    }, 150);
  },
  data() {
    return {
      type: "B",
      isShow: true,
    };
  },
};
</script>

<style></style>
