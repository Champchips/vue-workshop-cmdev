<template>
  <div id="Demo5">
    <h1>Demo5: Blinding</h1>
    <img v-bind:src="imageUrl" alt="" v-bind:height="height" />
    <br />
    <a v-bind:href="mywebUrl">My Website</a>
    <br />
    <a :href="mywebUrl">My Website</a>
    <div :class="[false ? error : important]">Blinding Class</div>
    <div :style="{ color, fontSize }">Blinding Style</div>
    <div :style="isActive ? styleObj : ''">Blinding Style Object</div>
    <button @click="isActive = !isActive">Toggle Active</button>
  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return {
      imageUrl: "https://i.ytimg.com/vi/U-C0I-Ks14M/maxresdefault.jpg",
      height: 200,
      mywebUrl: "https://github.com/Champchips",
      error: "error_class",
      important: "important_class",
      color: "green",
      fontSize: "30px",
      styleObj: {
        backgroundColor: "yellow",
        color: "green",
      },
      isActive: false,
    };
  },
};
</script>

<style>
.error_class {
  background-color: red;
  color: white;
}
.important_class {
  font-weight: bold;
}
</style>
